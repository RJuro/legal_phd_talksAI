# Title Slide
- **Slide title**: AI Benchmarks, Liability, and Legal Practice
- **Subtitle**: Ph.d-kursus i KI og jura
- **Speaker line**: Roman Jurowetzki · Associate Prof · AAU Business School · CAISA
- **Visuals**: Use AAU waves background (`\aauwavesbg`) with AAU rectangular logo.
- **Notes**: Keep metadata aligned with LaTeX preamble (title, subtitle, author, institute, date).

## Slide 0 – This is a field report (not legal advice)
- **Purpose**: Set stance as economist focused on patents, measurement, and AI tooling.
- **Slide copy**:
  - Hero text: “An outsider perspective”.
  - Footer block: “Economist → patents / innovation / tech dev • Measurement • AI tooling • AI policy” and “Leads MSc in Business Data Science”.
- **Visuals**: Minimalist layout, no meme; darker background acceptable.
- **Speaker notes**:
  - Emphasize field-audit mindset and validation focus.
  - Invite audience to treat talk as systems-level debrief, not doctrine.
  - Explicitly note “I am not a lawyer; I'm your auditor from the tech side.”
- **Sources**: none.

## Slide 1 – 24 months changed the job
- **Purpose**: Illustrate rapid shift from chat toy to integrated workflow tooling.
- **Slide copy**:
  - Bullets on agentic integration, enterprise adoption velocity, lagging governance.
  - Add points on capability leaps: coding copilots (“vibe coding”), competitive math results, expanding context windows, multimodal audio/video agents.
  - Call out emergence of structured outputs and reinforcement learning anchored to verifiable ground truth.
- **Visuals**:
  - Placeholder timeline graphic (“2023 → 2025 MCP milestones”).
  - Meme cue: “This is fine” reinterpretation.
  - Optional chart contrasting 2023 frontier models vs 2024/25 small models running locally.
- **Speaker notes**:
  - Highlight MCP as connective tissue for enterprise workflows.
  - Stress mismatch between deployment speed, capability blooms, and oversight.
  - Mention expectation-setting around structured outputs enabling automated QC.
- **Sources**: `mcp_site`, `anthropic_mcp`, `windows_mcp`.
- **Additional refs**: `phi3_blog`, `gpt4o_release`, `claude35_sonnet`, `gemini_longcontext`.

## Slide 2 – Capability ↑ vs Reliability ↔
- **Purpose**: Frame the capability-reliability gap and resulting liability zone.
- **Slide copy**:
  - Bullets on LLM breadth, reliability plateaus, humans as accountability.
- **Visuals**:
  - Placeholder dual-curve chart with shaded “Liability Zone”.
  - Meme cue: Spider-Man pointing (“useful” vs “trustworthy”).
- **Speaker notes**:
  - Explain steep capability curve vs flat reliability improvement.
  - Position the gap as legal practitioners’ workload.
- **Sources**: `gemini_longcontext`, `claude35_sonnet`, `gpt41_openai`, `openai_deep_research`, `jagged_frontier`.


## Slide 3 – How to work with it
- **Purpose**: Establish zero-trust intern workflow mindset.
- **Slide copy**:
  - Bullets: require sources, retain sign-off, design validation checklists.
  - Prompt the question: “Who actually knows enough to judge the output?”
  - Introduce “working with wizards” framing and obligation to demand reasons.
- **Speaker notes**:
  - Reinforce that models remain tools; accountability is human.
  - Emphasize knowledge ownership and keeping expertise sharp.
  - Reference Mollick “Working with Wizards” for cultural framing.
- **Sources**: `hai_hallucination`, `mollick_wizards`.

## Slide 4 – Three lazy takes to retire
- **Purpose**: Dismiss recurring simplistic narratives (autocomplete, bans, bar exam).
- **Slide copy**: Three column layout with:
  - “Autocomplete? Not anymore.”
  - “Just ban it.”
  - “Ignore emerging capabilities?”
- **Visuals**: Minimalist icons per phrase; optional meme-lite imagery emphasising resilience.
- **Speaker notes**:
  - Clarify why each “lazy take” fails (capability leaps, resilience building, structured outputs).
  - Mention emerging capabilities beyond text completion.
- **Sources**: optional callout `stanford_legal_hallucination`, `phi3_blog`.

## Slide 5 – Benchmarks are power tools
- **Purpose**: Position benchmarks as policy levers that drive delegation and procurement.
- **Slide copy**:
  - Bullets on defining “good enough”, shifting labor, exposing liability.
  - Explicit call-out that maintaining evaluation suites is a sovereign capability.
- **Visuals**: lederboards and benchmark result tests here
- **Speaker notes**:
  - Benchmarks move from trivia to governance instruments.
  - Stress building institutional capacity to maintain and refresh evaluation suites.
- **Sources**: `legalbench_site`, `lexglue_paper`, `coliee_site`.

The ability to maintain benchmarks is perhaps what is important to develop in orgs. and nationally?

## Slide 6 – Measure what matters to law
- **Purpose**: Distinguish performance metrics from liability metrics.
- **Slide copy**:
  - Two-column checklist (performance vs liability).
- **Visuals**: No major visuals; rely on typographic contrast and short sub-bullets per column.
- **Speaker notes**:
  - Stress need for citation fidelity, provenance, audit cost.
  - Give concrete liability metric examples (e.g., retrieval coverage, supervision hours).
- **Sources**: `large_legal_fictions`.

## Slide 7 – Why leaderboards lie
- **Purpose**: Warn about contamination and benchmark drift.
- **Slide copy**:
  - Bullets on leakage, overfitting, need for dynamic sandboxes.

introduce a bit more to train/test thinking in ML here.

- **Speaker notes**:
  - Encourage audience to demand rotating/evolving evaluation sets.
- **Sources**: `leak_cheat_repeat`, `contamination_forget`.

What klind of benchmarks do we need then?

## Slide 8 – Sovereignty = evaluation labs
- **Purpose**: Reframe AI sovereignty as evaluation capacity, not homegrown models.
- **Slide copy**:
  - Bullets on criteria → tests → red team → procurement pipeline.
- **Visuals**: Four-layer pyramid graphic placeholder.
- **Speaker notes**:
  - Tie to EU AI Act timeline and institutional build-out.
- **Sources**: `eu_ai_act_overview`, `eu_ai_act_timeline`.
this is just conceptual do not cite EU...

## Slide 9 – AI now does things
- **Purpose**: Show transition from chatbot to agentic actor via MCP.
- **Slide copy**:
  - Bullets on MCP, workflow automation, governance needs.
  - Caption prompt: “WHO APPROVED THIS?”
- **Visuals**: Flow diagram (Reg change → AI draft → staged deployment).
- **Speaker notes**:
  - Stress approvals, authentication, and audit log design.
- **Sources**: `mcp_site`, `windows_mcp`, `copilot_studio_mcp`.

only cite one anthropic one.

## Slide 10 – Logs > vibes
- **Purpose**: Advocate for audit rails baked into tooling.
- **Slide copy**:
  - Bullets on capturing inputs, sources, tool calls, outputs, sign-off.
- **Visuals**: Checklist icons for each tracked element.
- **Speaker notes**:
  - Connect to regulatory expectations for exportable logs.
- **Sources**: none.

Also mention: YEs, but does that help if we don't have org. capacity to use that or are owerwhelmed?

## Slide 11 – Rules you can run
- **Purpose**: Introduce Law/Rules as Code concept.
- **Slide copy**:
  - Bullets on ambiguity reduction, simulation readiness, cross-disciplinary review.
  - Split panel placeholder “Human text || Executable logic”.
- **Visuals**: Side-by-side panel graphic.
- **Speaker notes**:
  - Emphasize paired drafting to maintain fidelity.
- **Sources**: `better_rules_nz`, `oecd_rules_code`.

## Slide 12 – It’s already happening
- **Purpose**: Provide concrete Catala and OpenFisca exemplars.
- **Slide copy**:
  - Catala bullets: DSL, exceptions, verification.
  - OpenFisca bullets: microsim, policy prototyping.
- **Visuals**: Badge placeholders for each tool.
- **Speaker notes**:
  - Encourage audience to explore open tooling ecosystems.
  - Catala: emphasise exception handling, audit trails, French tax benefits example.
  - OpenFisca: mention French government usage, OECD pilots, ability to fork for local policy labs.
- **Sources**: `catala`, `openfisca`, `openfisca_docs`.

## Slide 13 – Test before it governs
- **Purpose**: Sell “unit-testing society” idea.
- **Slide copy**:
  - Bullets on synthetic populations, simulations, catching discrimination.
  - Caption: “WHO GETS DENIED AT THE EDGES?”
- **Visuals**: No major visuals; rely on bold caption.
- **Speaker notes**:
  - Link to computational law testing practices (CUTECat reference).
- **Sources**: `cutecat`.

## Slide 14 – Law as complex system
- **Purpose**: Explain opacity born from deterministic but intricate rule interactions.
- **Slide copy**:
  - Bullets on emergent behaviour, exceptions, need for telemetry.
- **Visuals**: Dual boxes “LAW (complex system)” vs “LLM (statistical)”.
- **Speaker notes**:
  - Reinforce measurement at system level, not clause level.
- **Sources**: none.

## Slide 15 – Already normal in biglaw workflows
- **Purpose**: Show industry adoption with guardrails.
- **Slide copy**:
  - Bullets on A&O + Harvey rollout, Westlaw/Lexis assistants, client expectations.
- **Visuals**: Generic firm/vendor logo placeholders.
- **Speaker notes**:
  - Stress that professional norms already assume augmented teams; you're not covering doctrinal detail.
  - Define “human review” as accountable partner-level sign-off, escalation protocols, and client disclosure.
- **Sources**: `reuters_harvey1`, `reuters_harvey2`, `tr_westlaw_launch`, `tr_cocounsel_integration`.

## Slide 16 – You still sign it
- **Purpose**: Highlight sanctions and verification duty.
- **Slide copy**:
  - Bullets on Mata v. Avianca, judicial certifications, fake-citation incidents.
  - Red “YOU STILL SIGN IT” stamp placeholder.
- **Visuals**: Custom stamp graphic on slide.
- **Speaker notes**:
  - Use as motivator: courts already sanction misuse; then pivot back to systems view.
- **Sources**: `mata_v_avianca`, `washingtonpost_hallucinations`, `businessinsider_fakecites`.


## Slide 17 – EVALUATE • BENCHMARK • SIMULATE
- **Purpose**: Present research agenda for the audience.
- **Slide copy**:
  - Enumerated actions: liability benchmarks, evaluation sandboxes, RaC + simulation prototype.
  - Large typographic treatment of the three verbs.
- **Visuals**: Bold lettering animation/graphic.
- **Speaker notes**:
  - Invite collaboration; reference open communities (LegalBench, Catala, OpenFisca).
  - Encourage focus on compliance, procurement standards, and responsible adoption infrastructure beyond restriction.
- **Sources**: `legalbench_site`, `lexglue_paper`, `catala`, `openfisca`.


## Slide 18 – If you had to choose…
- **Purpose**: Seed Q&A around benchmark ownership and liability focus.
- **Slide copy**:
  - Two large buttons: Performance (unchecked) vs Liability (checked).
  - Bullet prompts for discussion (benchmarks authorship, audit trail, negligence threshold).
- **Visuals**: High-contrast button pair.
- **Speaker notes**:
  - Use to transition into audience discussion.
- **Sources**: none.

## Slide 19 – References
- **Purpose**: Provide bibliography compiled via `biblatex`.
- **Slide copy**: Standard `\printbibliography` output using `references.bib`.
- **Notes**: Ensure all citations in slides map to BibTeX keys listed above; update both LaTeX and this document when adding/removing sources.
