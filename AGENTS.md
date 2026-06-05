# Codex Project Instructions

## Read first

Before editing, read `PROJECT_CONTEXT.md`, `README.md`, and `DEPLOYMENT_GUIDE_CN.md`.

## Project goal

Maintain a bilingual public static simulator for the 碳行家 / Carbon Navigator Tencent Ads research funnel.

## Technical constraints

- Use plain HTML, CSS, and JavaScript unless the user explicitly requests a framework.
- Keep the project deployable on GitHub Pages without a build step.
- Preserve all three language modes: bilingual, Chinese-only, and English-only.
- All user-facing strings must be added to the translation dictionary in `app.js`.
- Keep observed data visually and logically separate from editable scenario assumptions.
- Do not claim scenario multipliers are causal estimates.
- Run a local syntax check after JavaScript changes.
- Do not add analytics trackers, cookies, external fonts, or third-party scripts without explicit approval.

## Privacy and security

Never commit or display:

- API keys or secrets
- participant names or contact details
- OpenIDs
- CloudBase JSON/JSONL exports
- raw survey responses
- private research reports or identifiable screenshots

The public site should contain aggregate, de-identified values only.

## Preferred workflow

1. Inspect the relevant files.
2. Explain the intended change briefly.
3. Edit the smallest necessary set of files.
4. Check syntax and basic page loading.
5. Summarize changed files and remaining assumptions.
