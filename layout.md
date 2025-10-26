AAUsimple Beamer layout specs
================================

Document defaults
-----------------
- Class: `beamer` with `10pt` base font and `aspectratio=169`.
- Theme loader: `\usetheme[]{AAUsimple}` which pulls `beamerthemeAAUsimple.sty` plus inner, outer, and color theme companions.
- Core packages: `tikz` (`shapes.geometric`, `arrows`, externalization helpers), `calc`, `fp`, `helvet`, `babel` (english), `inputenc` utf8, `fontenc` T1, and `biblatex` (authoryear, `biber`).

Color system
------------
- Primary brand colors (from `beamercolorthemeAAUsimple.sty`):
  - `beamer@barcolor` = RGB(194,193,204)
  - `beamer@headercolor` = RGB(33,26,82)
  - `beamer@normaltextcolor` = RGB(84,97,110)
- Presentation frames use `AAUsimple` color pair (`fg` = bar color, `bg` = header color). Structure elements inherit the header blue.
- Secondary palette in the deck body (declared in `AAUsimpletheme.tex`):  
  `aauDarkOrange` RGB(187,91,23), `aauDarkGold` RGB(151,112,31), `aauDarkBlue` RGB(0,127,163), `aauDarkGreen` RGB(14,133,99), `aauLightBlue` RGB(49,169,193) for emphasis and block accents.

Typography and spacing
----------------------
- Helvetica is the main text face (`\usepackage{helvet}`) rendered through T1 encoding.
- Frame titles sit inside a minipage whose height equals `2.5 ×` the frametitle line height, ensuring breathing room above content.
- Subtitle, author, date, and institute text on the title slide inherit beamer defaults but are wrapped inside a centered `beamercolorbox` with the frametitle palette.

Header, navigation, and progress
--------------------------------
- Header bar (`\aauheaderbackground`) renders a full-width rectangle in AAU blue with a circular cut-out hosting the AAU round logo (`AAUgraphics/aau_logo_new_circle`).
- Circular progress indicator wraps around the logo area. Options (set via theme keys):
  - `progressstyle=fixedCircCnt` (default) shows a single moving arc and current frame number.
  - `progressstyle=movCircCnt` adds both total and current frame markers.
  - `progressstyle=corner` falls back to the default beamer footline counter.
- Optional switches:
  - `rotationcw` flips progress rotation direction to clockwise.
  - `shownavsym` re-enables navigation symbols; omitted by default for a clean look.
- Footline is empty unless `progressstyle=corner` is used; headline displays `\insertshortauthor | \insertshorttitle`.

Title and closing frames
------------------------
- Title template: full-height minipage with stacked title, subtitle, date, author, institute, and `\titlegraphic` (AAU rectangular logo). Designed for use with the `\aauwavesbg` overlay (see below).
- Final slide helper: `\finalpage{<text>}` macro draws a frametitle-colored box centered on the slide with customizable closing text and the AAU logo beneath.

Background and imagery
----------------------
- `\aauwavesbg` macro injects `AAUgraphics/aau_waves` as the background canvas and applies a semi-transparent white overlay (75% opacity) to keep text legible.
- All logos and wave assets (EPS + PDF) live in `AAUgraphics/` for inclusion in both latex and pdf workflows.

Content styling aids
--------------------
- Bibliography items use the text label style (`\setbeamertemplate{bibliography item}[text]`) to match the minimalist look.
- Blocks and columns inherit the color theme, with additional semantic colors defined in the TeX source for emphasis.
- TikZ diagram on the “Methodological Engine” slide relies on the theme’s `tikzexternaldisable` / `enable` calls to avoid interference with externalization passes.
- Custom hyperlink command `\chref{<url>}{<label>}` is provided to keep links consistent with the AAU color palette.

Slide composition best practices
--------------------------------
- Columns: Use `\begin{columns}[T]` to top-align content; two columns at `0.48\textwidth` maintain comfortable gutters in the 16:9 layout. Reserve three-column grids for compact blocks or infographics.
- Blocks: Prefer the standard `block`, `alertblock`, and `exampleblock` environments instead of ad-hoc formatting; they automatically adopt the theme colors. Apply secondary palette colors sparingly via `\textcolor{aauDarkBlue}{…}` for emphasis.
- Layering: Combine `columns` with `\vfill` above/below sections to balance white space and prevent crowding against the header.
- Progressive reveal: Use `\pause` between bullet items or columns when presenting live to keep attention focused; avoid overusing it in dense data slides.
- Graphics: Center diagrams within columns using `\centering` and wrap wide figures in a single-column frame to preserve readability on projector resolutions.

Compilation workflow
--------------------
- `Makefile` target `make pdflatex` runs:  
  `pdflatex -shell-escape` → `biber` → two more `pdflatex -shell-escape` passes, then removes auxiliary files (`*.aux`, `*.nav`, `*.snm`, etc.).
- `-shell-escape` is required for TikZ externalization used by the theme background helpers.
- `make clean` deletes intermediate files plus the generated PDF.

Usage tips
----------
- Call `\aauwavesbg` immediately before the title frame to apply the branded background. Leave subsequent frames without it unless a full-bleed look is needed.
- Supply `\titlegraphic{\pgfuseimage{titlepagelogo}}` after declaring `\pgfdeclareimage` so the theme can reuse the logo on title and final slides.
- Add `\addbibresource{references.bib}` before `\begin{document}`; run `biber` between LaTeX passes to populate references.
- Cite in-text with `\parencite{key}` for parenthetical references and `\textcite{key}` for narrative mentions so the bibliography slide auto-updates.
- Keep per-frame bibliography usage minimal; redirect detailed citations to the final `allowframebreaks` reference slide.
- When mixing text and data tables, let text lead the slide and keep tables in landscape or dedicated frames to avoid shrinking font sizes below theme defaults.
