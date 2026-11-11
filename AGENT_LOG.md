# Agent log

Add a dated entry each time you work with your AI coding agent, with the newest entry at the bottom. Each entry records what you asked the agent, what it produced, and what you checked or changed. Paste your key prompts in exactly as you typed them. Include at least one time the agent got something wrong, and how you caught it.

Copy this outline for each entry:

```markdown
## YYYY-MM-DD: What you worked on

- **Asked:** "Paste your prompt here."
- **Agent produced:** What it made or changed.
- **Checked or changed:** How you checked it, and what you fixed.
```

## 2026-11-11: Building the first College-Town Home Sales Explorer

- **Asked:** "Read AGENTS.md and docs/data_description_sheet.md first.\n\nReplace the placeholder page with a simple, polished English-language website titled “College-Town Home Sales Explorer,” using data/college_town_home_sales.csv.\n\nFor this first version:\n- Show a horizontal bar chart comparing median sale prices by city and state.\n- Include a table with each city/state, its eligible sale count, and median sale price.\n- For all price statistics and sale counts, include only sales from $10,000 through $5,000,000, inclusive. Clearly explain this filtering rule on the page.\n- Compute every displayed statistic from the dataset. Do not invent numbers or deduplicate by street address.\n- Use plain HTML, CSS, and JavaScript, with relative file paths compatible with the existing GitHub Pages workflow.\n- Do not modify any of the five original dataset files.\n- Include the dataset citation from the data description sheet.\n- Make the page readable on desktop and mobile.\n- Record this task and the work performed in AGENT_LOG.md.\n\nImplement only this first version. Explain your plan before making changes, and afterward tell me how to check the result."
- **Agent produced:** Replaced the placeholder with a responsive single-page explorer that fetches the CSV, parses quoted fields, filters eligible prices, computes city/state counts and medians, and renders an SVG chart and accessible table. Added the filtering explanation, dataset citation, and relative documentation link.
- **Checked or changed:** The first implementation draft used a simple comma split for CSV rows, which would have broken quoted values such as university names containing commas. I caught that during review of the CSV sample and replaced it with a quote-aware parser before finalizing. The five original files in `data/` were left untouched.
