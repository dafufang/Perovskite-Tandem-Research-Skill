# Perovskite Tandem Research Skill (English Introduction)

## Overview

`perovskite-tandem-research` is a research analysis Skill for perovskite and tandem solar cell R&D. It supports academic literature review, paper analysis, research trend scanning, efficiency record verification, technology route comparison, experiment planning, commercialization assessment, competitor/institution tracking, and R&D decision support for companies, laboratories, or research organizations.

The Skill is not designed as a large static paper database that quickly becomes outdated. Instead, it provides reusable domain frameworks, representative literature maps, metric definitions, stability assessment rules, technology route evaluation methods, and update rules for verifying current information through web sources.

## Use Cases

Use this Skill for tasks such as:

- Reviewing papers on perovskite solar cells, perovskite/silicon tandems, all-perovskite tandems, and related photovoltaic technologies
- Summarizing recent progress, research hotspots, and bottlenecks in a specific direction
- Comparing 2T vs 4T tandems, perovskite/silicon vs all-perovskite tandems, solution processing vs vapor deposition, and other technical routes
- Verifying latest efficiency records, certified results, company announcements, and commercialization status
- Designing experimental validation plans, test matrices, stability tests, and Go/No-Go criteria
- Supporting internal R&D decisions for companies, laboratories, or research institutions
- Tracking public progress from organizations such as Oxford PV, LONGi, HZB, KAUST, NREL, and Fraunhofer ISE

## Main Workflow Modes

### 1. paper-review

Use this mode for uploaded papers, named papers, DOI/title analysis, or questions about “this paper.” The default output includes:

- One-sentence judgment
- Research background
- Device architecture
- Key novelty
- Performance data
- Stability analysis
- Data credibility
- Reproducibility assessment
- Scale-up and commercialization relevance
- R&D implications
- Suggested validation experiments

### 2. research-scan

Use this mode for questions about recent progress, research trends, hotspots, and future opportunities. The default output includes:

- Overall judgment
- Latest progress
- Technical hotspots
- Core bottlenecks
- Representative papers
- Representative institutions/companies
- Commercialization signals
- Topics worth following
- Topics to deprioritize

If the user asks about “latest,” “recent,” “current,” “this year,” efficiency records, or company updates, the Skill requires up-to-date web verification.

### 3. route-evaluation

Use this mode to compare technology routes such as:

- perovskite/silicon 2T tandem
- perovskite/silicon 4T tandem
- all-perovskite tandem
- perovskite/CIGS tandem
- wide-bandgap perovskite top cell
- Sn-Pb low-bandgap bottom cell
- slot-die coating
- vapor deposition
- textured-silicon-compatible processes

The default output includes route comparison, efficiency potential, stability risks, process compatibility, scale-up difficulty, cost and equipment requirements, competitive landscape, and recommended priority.

### 4. rd-decision

Use this mode for direction selection, project initiation, investment assessment, or internal R&D prioritization. The default output includes:

- Go / Conditional Go / Watch / No-Go conclusion
- Key assumptions
- Key risks
- Resource requirements
- Three-month validation experiments
- Six-month milestones
- Go/No-Go criteria

### 5. experiment-planning

Use this mode to convert a paper, route, or R&D question into an executable experiment plan. The default output includes:

- Experiment objective
- Core hypothesis
- Sample architecture
- Variable design
- Control groups
- Fabrication workflow
- Characterization plan
- Stability testing plan
- Success criteria
- Failure criteria
- Fallback plans

### 6. competitor-watch

Use this mode to track companies, institutions, certified efficiencies, modules, pilot lines, and commercialization progress. This mode must verify current facts with web sources rather than relying only on static references.

## Directory Structure

```text
perovskite-tandem-research/
├── SKILL.md
├── README_CN.md
├── README_EN.md
├── agents/
│   └── openai.yaml
└── references/
    ├── workflow.md
    ├── literature-map.md
    ├── key-papers.md
    ├── literature-update-rules.md
    ├── paper-review-template.md
    ├── technology-routes.md
    ├── route-evaluation-framework.md
    ├── rd-decision-framework.md
    ├── experiment-planning.md
    ├── stability-assessment.md
    ├── metrics-glossary.md
    ├── source-priority.md
    ├── competitor-watchlist.md
    ├── manufacturing-and-scaleup.md
    ├── go-no-go-scorecard.md
    └── report-template.md
```

## Reference Files

- `workflow.md`: task mode selection and routing logic
- `literature-map.md`: literature map for perovskite and tandem solar cells
- `key-papers.md`: representative paper cards
- `literature-update-rules.md`: rules for searching, screening, updating, and citing literature
- `paper-review-template.md`: structured paper review template
- `technology-routes.md`: technology route knowledge base
- `route-evaluation-framework.md`: route evaluation framework
- `rd-decision-framework.md`: internal R&D decision framework
- `experiment-planning.md`: experiment planning templates
- `stability-assessment.md`: stability and reliability assessment rules
- `metrics-glossary.md`: definitions of photovoltaic and tandem metrics
- `source-priority.md`: source priority and credibility rules
- `competitor-watchlist.md`: watchlist for companies and research institutions
- `manufacturing-and-scaleup.md`: manufacturing, module, and scale-up checklist
- `go-no-go-scorecard.md`: reusable weighted Go/No-Go scorecards
- `report-template.md`: templates for research and decision reports

## Core Evaluation Principles

The Skill explicitly distinguishes:

- Certified efficiency vs self-reported efficiency
- Active area vs aperture area vs designated illumination area vs module area
- Scan PCE vs stabilized PCE vs MPP-tracked output
- Lab-scale cells vs minimodules vs commercial modules
- Short-term storage stability vs operational reliability
- Unencapsulated vs encapsulated stability
- Indoor STC results vs outdoor energy yield
- Paper results vs manufacturable processes
- Company announcements vs third-party verified results

## Example Prompts

```text
Review this perovskite/silicon tandem paper and focus on novelty, stability, and commercialization relevance.
```

```text
Compare 2T and 4T perovskite/silicon tandem routes and provide an R&D priority and Go/No-Go judgment.
```

```text
What are the latest important developments in all-perovskite tandem solar cells? Separate academic progress from commercialization progress.
```

```text
Based on this paper, design a three-month validation experiment for a wide-bandgap perovskite top cell.
```

```text
Track the latest public progress from Oxford PV and LONGi in perovskite/silicon tandems and assess credibility.
```

## Important Limitations

- Static references are used for frameworks, terminology, and representative literature leads. They should not be treated as current facts.
- Latest papers, efficiency records, certification status, company updates, and commercialization progress must be verified with up-to-date sources.
- Company press releases and marketing materials should not be treated as equivalent to third-party certification or commercial maturity.
- High-efficiency small-area cells in papers should not be treated as equivalent to manufacturable modules.
- This Skill contains no internal information from any specific company unless the user explicitly provides such information in the current conversation.

## Installation and Deployment Guide

The standard deliverable for this Skill is `perovskite-tandem-research.zip`. Different agent tools support Skills in different ways. Some tools can upload the ZIP directly, while others should use `SKILL.md` and the `references/` folder as project instructions, knowledge files, or RAG sources.

### 1. Native ChatGPT Skills Installation

Use this path if your ChatGPT workspace supports native Skill uploads.

1. Open the Skills management page or Skills Library in ChatGPT.
2. Choose upload or create Skill.
3. Upload `perovskite-tandem-research.zip`.
4. Confirm that the Skill name is `perovskite-tandem-research`.
5. Test with the prompt below:

```text
Compare perovskite/silicon 2T tandem and all-perovskite tandem as R&D priorities.
```

A successful response should include route comparison, stability risks, commercialization judgment, and a Go / Conditional Go / Watch / No-Go conclusion.

### 2. ChatGPT Custom GPT / GPT Builder

Custom GPTs may not run a ChatGPT Skill ZIP as a native Skill, but the package can be used as instructions and knowledge files.

Recommended steps:

1. Unzip `perovskite-tandem-research.zip`.
2. Create a new GPT in GPT Builder.
3. Copy the core behavior rules from `SKILL.md` into Instructions.
4. Upload the Markdown files in `references/` as Knowledge.
5. Optionally upload `README_CN.md` and `README_EN.md` as user documentation.
6. Enable Web browsing / Search if available, because this Skill requires current verification for papers, records, and company updates.
7. Test with:

```text
What are the latest public developments from Oxford PV and LONGi in perovskite/silicon tandems? Separate self-reported claims from third-party certified information.
```

### 3. OpenAI Assistants / Responses API Agent

Use this path for a custom OpenAI Agent, RAG Agent, or internal research assistant.

Recommended deployment:

1. Unzip `perovskite-tandem-research.zip`.
2. Put the contents of `SKILL.md` into the agent's system/developer instructions.
3. Load the `references/` files into a vector store or file search system.
4. Keep `README_CN.md` and `README_EN.md` as user-facing documentation.
5. Configure Web search or an external retrieval tool for current fact checking.
6. Add routing rules:
   - For paper reviews, retrieve `paper-review-template.md`, `metrics-glossary.md`, and `stability-assessment.md`.
   - For route evaluation, retrieve `technology-routes.md` and `route-evaluation-framework.md`.
   - For latest efficiency records, company updates, and commercialization status, call Web search.

Suggested test prompt:

```text
Based on recent public information, assess whether perovskite/silicon tandem technology is ready for commercialization and rate the evidence level.
```

### 4. Claude Projects

Claude Projects may not natively install a ChatGPT Skill ZIP, but the package can be used as Project Knowledge.

Recommended steps:

1. Unzip `perovskite-tandem-research.zip`.
2. Create a Claude Project.
3. Add `SKILL.md` to Project Instructions or project-level guidance.
4. Upload the `references/` files as Project Knowledge.
5. Upload `README_CN.md` and `README_EN.md` as documentation.
6. If current facts are needed, use a Claude environment with web access or provide current sources manually.

### 5. Gemini Gems

Gemini Gems generally use custom instructions and knowledge files.

Recommended steps:

1. Unzip `perovskite-tandem-research.zip`.
2. Create a Gem.
3. Put the core rules from `SKILL.md` into Gem Instructions.
4. Upload the `references/` files as knowledge materials.
5. If web access is available, instruct the Gem to verify current papers, efficiency records, and company developments before making factual claims.

### 6. Cursor / Windsurf / Cline / Roo Code and Similar Coding Agents

These tools are usually better suited to project-level agent instructions rather than native Skill installation.

Recommended project structure:

```text
project-root/
├── .agent/
│   └── perovskite-tandem-research/
│       ├── SKILL.md
│       ├── README_CN.md
│       ├── README_EN.md
│       └── references/
└── AGENTS.md or CLAUDE.md or .cursorrules
```

Deployment steps:

1. Unzip `perovskite-tandem-research.zip` into `.agent/perovskite-tandem-research/`.
2. Add the following instruction to `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, or the equivalent rules file:

```text
When the task concerns perovskite solar cells, perovskite/silicon tandems, all-perovskite tandems, PV efficiency records, stability, scale-up, manufacturing, or photovoltaic R&D strategy, follow .agent/perovskite-tandem-research/SKILL.md and consult the references folder as needed.
```

3. Enable browser or MCP search tools if available.
4. If the tool has no web access, use the Skill only for structured analysis and do not claim that current facts have been verified.

### 7. Dify / Coze / LangChain / LlamaIndex Workflow Agents

Use this path for RAG or multi-step research agents.

Recommended deployment:

1. Unzip `perovskite-tandem-research.zip`.
2. Use `SKILL.md` as the system prompt or application-level instruction.
3. Import the `references/` files into the knowledge base and preserve filenames as metadata.
4. Set up retrieval routing:
   - `paper-review`: retrieve `paper-review-template.md`, `metrics-glossary.md`, `stability-assessment.md`.
   - `research-scan`: retrieve `literature-map.md`, `key-papers.md`, `literature-update-rules.md`.
   - `route-evaluation`: retrieve `technology-routes.md`, `route-evaluation-framework.md`.
   - `rd-decision`: retrieve `rd-decision-framework.md`, `go-no-go-scorecard.md`.
   - `experiment-planning`: retrieve `experiment-planning.md`, `stability-assessment.md`.
   - `competitor-watch`: retrieve `competitor-watchlist.md`, `source-priority.md`, then call Web search.
5. Add a Web search node for current fact checking and require cited outputs.

### 8. Local Folder Usage

For manual use without a platform-specific installation:

1. Unzip `perovskite-tandem-research.zip`.
2. Open `SKILL.md` and provide its core rules to the model.
3. Provide the relevant `references/` files together with the task.
4. For current facts, use a model with web access or manually provide up-to-date sources.

## Post-Installation Validation Checklist

After installation, test the following:

```text
1. Review a perovskite/silicon tandem paper.
2. Compare 2T and 4T perovskite/silicon tandem routes.
3. Design a three-month experiment plan for a wide-bandgap perovskite top cell.
4. Verify a company's latest perovskite/silicon tandem efficiency record.
5. Provide a Go / Conditional Go / Watch / No-Go judgment for a technology route.
```

A correct setup should:

- Output Chinese by default unless instructed otherwise.
- Ask for or perform web verification for current facts.
- Distinguish certified efficiency from self-reported efficiency.
- Distinguish small-area cells, minimodules, and commercial modules.
- Check encapsulation, MPP tracking, light intensity, temperature, humidity, and test duration for stability claims.
- Provide Go / Conditional Go / Watch / No-Go judgments for R&D decisions.

## Maintenance Recommendations

- Update `key-papers.md` and `competitor-watchlist.md` monthly.
- Update `technology-routes.md`, `route-evaluation-framework.md`, and `go-no-go-scorecard.md` quarterly.
- Whenever a new certified efficiency record or major company development appears, update the search hints in `literature-update-rules.md` or add a new paper/company card.
- Avoid embedding large full-text papers directly in the Skill. Prefer structured paper cards and dynamic retrieval rules.
