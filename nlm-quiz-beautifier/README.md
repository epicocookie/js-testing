# NLM Quiz Beautifier ✦

A tiny, dependency-free browser tool for restyling interactive HTML quizzes exported from NotebookLM-style quiz exporters.

## What it does

1. Drop in an exported `.html` quiz.
2. Pick a visual theme.
3. Preview the result in a sandboxed iframe.
4. Download a new themed `.html` file.

The tool **does not rewrite the questions, answers, data attributes, or existing quiz JavaScript**. It injects an additional CSS theme at the end of the document so the original behavior remains intact.

## Included themes

- **Focus** — Notion × Linear inspired study UI
- **Midnight** — dark, high-contrast study mode
- **Paper** — warm textbook look
- **Mint** — calm light green theme

## Privacy

Everything happens locally in the browser. The selected quiz file is not uploaded to a server.

## Run it

No install. No build step.

```text
open index.html
```

Or serve the directory with any static server.

## Compatibility

The current theme selectors target the common structure used by exported interactive quizzes with classes such as:

- `.container`
- `.header`
- `.progress-bar` / `.progress-fill`
- `.question`
- `.q-text`
- `.option`
- `.option-feedback`
- `.hint-box`
- `.next-btn`
- `.results`

If an exporter changes those class names, the file still loads, but some visual rules may not apply.

## Design principle

**Reskin the quiz. Keep the brains.**

The beautifier is intentionally CSS-first so it does not need to understand or regenerate the quiz logic.
