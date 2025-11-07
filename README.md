# From Engineer to Architect: Facilitating High-Impact Decisions

This repository contains a 90-minute interactive workshop designed for engineers transitioning into architecture roles. The session focuses on **how architects enable critical technical decisions**, not by dictating solutions, but by **facilitating clarity, framing trade-offs, and aligning stakeholders**.

The workshop includes short concept segments, followed by three real-world architecture scenarios that participants work through in small breakout groups.

## Learning Objectives

By the end of this session, participants should be able to:

- Shift from **solution provider** to **decision facilitator**
- Use a **lightweight decision framing template** to structure complex decisions
- Surface and articulate key **trade-offs** instead of optimizing for a single dimension
- Balance **technical**, **organizational**, and **strategic** concerns
- Guide a group toward **shared understanding and aligned action**


## Presenting the Slides

This presentation is built using **Marp**.

### Present in VS Code

1. Install **Marp for VS Code**:  
   https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode

2. Open:
   ```
   decisions.md
   ```

3. Open Marp Preview:
   ```
   Cmd/Ctrl + Shift + P → "Marp: Open Preview"
   ```

4. Choose **Presenter View** for speaker notes.

## Generating a PDF

You can export from VS Code or via CLI.

### Export from VS Code

From the Marp preview window:
```
Export → PDF
```

### Export via CLI

```bash
npm install -g @marp-team/marp-cli
marp decisions.md --pdf --allow-local-files
```

This generates:
```
decisions.pdf
```

## Running the Workshop

| Segment | Duration | Format |
|---|---|---|
| Concept intro & framing | 10 min | Facilitated |
| Scenario 1 | 25 min | Introduce → Breakout → Share back |
| Scenario 2 | 25 min | Introduce → Breakout → Share back |
| Scenario 3 | 25 min | Introduce → Breakout → Share back |
| Key takeaways & close | 5 min | Facilitated |

## Contributions

Improvements and scenario suggestions are welcome. Submit a PR or open an issue.

## Attribution

All illustration assets were generated custom for this workshop and may be reused in your organization.
