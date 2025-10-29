Agents Manual
=============

## Mission
- Build and maintain a Shiny for Python dashboard that compares observed disease cases with Google Trends search interest to assess predictive value.
- Ensure the dashboard remains deployable via Shinylive to GitHub Pages and accessible to non-technical stakeholders.

## Deliverable Snapshot
- Product: Interactive Shiny for Python dashboard bundled for Shinylive deployment.
- Capabilities: Compare one or more trend terms with disease-case series, show predictive indicators (correlations, lead/lag views, basic forecasts).
- Audience: Analysts and public health observers; AI agents serve as primary maintainers.
- Constraints: Python-only preprocessing; UTF-8 (no BOM) text outputs; README stays concise yet expressive (emojis welcome).

## Data & Preprocessing
- Inputs: Disease case counts (time series) and Google Trends data (time series by query term).
- Acquisition: Prefer Python scripts/notebooks for API pulls or CSV ingestion; store raw sources under `data/raw/` (create as needed).
- Processing: Implement transformations in Python (e.g., `pandas`, `polars`). Document steps in-code; export curated datasets to `data/processed/`.
- Reproducibility: Provide runnable scripts in `scripts/` or notebooks in `notebooks/`; include usage instructions or CLI entry points.

## Tooling & Environment
- Language: Python (align versions with project config; default to 3.11 if unspecified).
- Dashboard Framework: Shiny for Python (use `shiny` + `shinylive` tooling).
- Deployment: Produce static Shinylive bundle (`shinylive export ...`) and publish to GitHub Pages. Automate via GitHub Actions when feasible.
- Testing: Use lightweight smoke tests for data loaders and app modules; ensure dashboard starts locally before exporting.

## Core Workflows
### 1. Data Update
- Pull latest disease-case and Google Trends data.
- Run preprocessing scripts; validate schemas and date coverage.
- Commit updated processed data with change notes.

### 2. Analysis & Modeling
- Compute correlations, lag analysis, and simple predictive metrics.
- Surface key insights in the dashboard (plots, tables, narrative text).
- Keep heavy modeling optional; prioritize interpretable outputs.

### 3. Dashboard Iteration
- Structure Shiny app modules logically (e.g., `app.py`, `modules/`).
- Expose controls for term selection, date ranges, smoothing options.
- Provide responsive visualizations (line charts, heatmaps, correlation summaries).

### 4. Quality Assurance
- Run lint/format (e.g., `ruff`, `black`) if configured.
- Execute automated tests and manual exploratory checks of the UI.
- Verify exported Shinylive bundle loads offline before deploying.

### 5. Deployment
- Update version notes in `readme.md` when user-facing changes occur.
- Export via `shinylive export`. Commit bundle under `docs/` (or designated publish folder).
- Push changes; confirm GitHub Pages build succeeds.

## Collaboration Protocols
- Log every user prompt and agent response verbatim in `prompts.md`.
- Avoid destructive git commands; respect existing uncommitted changes.
- When uncertain about requirements, ask clarifying questions before editing.
- Prefer refactoring to bolting on complexity; encapsulate logic cleanly.

## Writing & Style
- Text files: UTF-8 without BOM; keep Markdown readable with clear headings.
- README: concise, inviting tone; feel free to add color with emojis when appropriate.
- Comments: add only when code intent is non-obvious; keep them succinct.

## Troubleshooting & Escalation
- If Shinylive export fails, confirm Shiny app imports resolve and dependencies are pinned.
- For data anomalies (missing dates, unexpected spikes), document findings in commit messages and notify via prompts.
- Escalate sandbox or permission issues using the CLI approval workflow; note justification clearly.

## Session Checklist
- [ ] Sync or pull latest trunk.
- [ ] Review `prompts.md` for context.
- [ ] Run relevant data pipelines/tests before dashboard edits.
- [ ] Validate dashboard locally after changes.
- [ ] Update documentation (`readme.md`, `agents.md`, others) to reflect new behavior.
- [ ] Commit with descriptive messages; tag significant releases if required.
