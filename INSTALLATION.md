# Use the GPT Prompt Command Library in AI Projects

## GitHub Pages

Follow the numbered publishing steps in the root `README.md`. Keep `index.html`, `app.js`, `styles.css`, `data/commands.json`, and `assets/favicon.svg` at their documented paths.

## ChatGPT Plus Project

1. Open your ChatGPT Project.
2. Add `SKILL.md` and `references/commands.md` as project files.
3. Add Project instructions: "For slash-style prompts, use the GPT Prompt Command Library files as conventions and produce the requested deliverable."
4. Test: `/cheatsheet Explain B2B SaaS lead scoring to a new marketing operations hire.`

## Custom GPT

In your custom GPT's configuration, provide the skill behavior in its Instructions and upload the reference catalog as Knowledge. Custom GPTs do not automatically register these strings as native UI slash commands.

## Claude Project or compatible skill environment

Upload `SKILL.md` and `references/commands.md` to a Claude Project, or adopt the `SKILL.md` folder structure in a compatible tool that supports Agent Skills. Installation specifics vary by client.

## Keep versions in sync

Your GitHub repository is the source of truth. AI Project copies remain unchanged until manually replaced or updated through a separately configured integration.
