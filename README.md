# GPT Prompt Command Library

A polished, **searchable GitHub Pages website** for 132 custom slash-style AI prompt commands, plus a portable `SKILL.md` and command reference for AI projects.

## What's included

- Searchable, filterable command cards across six collections
- **Click any command to open an explanation window** showing what it does, what the output includes, and an example
- Built-in prompt builder to personalize the command and copy a complete prompt
- Favorites saved **locally in your browser** (no user account or analytics)
- Mobile-friendly static site; no build step, package manager, or API key
- Portable AI skill instructions (`SKILL.md`) and full Markdown command catalog (`references/commands.md`)

> **Important:** These are custom shorthand prompts, **not official built-in ChatGPT slash commands**. Best results come from copying the complete generated prompt. The site does not call a language model.

## Publish to GitHub Pages — step by step

1. Open **https://github.com/new**.
2. Enter repository name **`gpt-prompt-command-library`**.
3. Choose **Public** for a public website (or use Private only if your GitHub plan supports Pages for private repositories).
4. Click **Create repository**.
5. Upload the files and folders in this repository **keeping the folder paths intact**. `index.html` must live in the repository root. If GitHub creates a README initially, replace or edit it with this one.
6. On GitHub, go to **Settings → Pages**.
7. Under **Build and deployment**, choose **Deploy from a branch**, select **main** and **/(root)**, then **Save**.
8. Open the Pages URL shown in Settings → Pages. For this repository name, it will generally be `https://YOUR-USERNAME.github.io/gpt-prompt-command-library/`.
9. Test search, category filters, a command card, and **Copy complete prompt**.

**Tip:** For best results, upload a ZIP using GitHub Desktop or git, since the GitHub web uploader may not preserve the intended folder hierarchy when selecting individual files. You can also create folders in the browser using filenames like `data/commands.json`.

## Structure

```text
gpt-prompt-command-library/
├── index.html                 # GitHub Pages website
├── styles.css                 # Responsive appearance
├── app.js                     # Search, modal, prompt builder, favorites
├── data/
│   └── commands.json         # All 132 commands, descriptions, examples
├── assets/
│   └── favicon.svg
├── SKILL.md                   # Portable AI skill instructions
├── references/
│   └── commands.md           # Human-readable command catalog
├── docs/
│   └── INSTALLATION.md       # ChatGPT / Claude project use
├── LICENSE
└── README.md
```

## Use in ChatGPT Plus Projects

Download or copy `SKILL.md` and `references/commands.md` into your Project's files. Add these Project instructions:

> Use the uploaded GPT Prompt Command Library to interpret custom slash-style prompts. Look up a command in `references/commands.md`, follow `SKILL.md`, and produce the actual requested deliverable rather than only a prompt, unless I ask for a prompt. Treat the commands as user-defined shortcuts, not official built-in commands.

**Updating the GitHub repository does not automatically update previously uploaded Project files.** Re-upload revised versions as needed.

## Adding new commands

1. Add an entry to `data/commands.json` with `command`, `category`, `summary`, `description`, `example`, and `output`.
2. Add the same command to `references/commands.md`.
3. Commit to the `main` branch; GitHub Pages will redeploy the static site.

No code edits are needed for new cards, categories, or details: `app.js` renders from the JSON catalog.

## Privacy and compatibility

All search, favorites, editing, and prompt construction happen in the browser. Favorites use browser `localStorage`; prompts are not transmitted. The clipboard API may require HTTPS or localhost (both are supported by GitHub Pages / standard local serving). Opening `index.html` directly from disk using `file://` may block the catalog fetch; publish to GitHub Pages or serve locally (for example, `python3 -m http.server 8000`).

## Attribution / license

MIT license. You can edit and extend the catalog freely under the license terms. The project does not claim affiliation with OpenAI, Anthropic, or GitHub.
