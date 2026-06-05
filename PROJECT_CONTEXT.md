# Project Context / 项目背景

## Project

- Chinese name: 碳行家
- English working name: Carbon Navigator
- Product: WeChat Mini Program for a carbon-behavior research project
- Research flow: users enter from Tencent Ads, consent/register, complete environmental-awareness and identity-related questions/tasks, and receive rewards.
- Primary problem: impressions and clicks are acceptable, but many users leave before completing the research tasks.

## Observed June 4, 2026 baseline

- Ad spend: ¥10,000
- Impressions: 7,829
- Clicks: 1,708
- In-app consents: 129
- Entry-survey completions: 85
- Final completions: 70
- Real advertising cost per final completer: about ¥142.86

## Core diagnosis

The platform-reported conversion count was nearly equal to clicks, so the optimization event appears too shallow. The simulator must distinguish click/open, consent, entry-survey completion, final completion, and quality-passed completion.

## Mini Program codebase

The uploaded Mini Program uses a native WeChat structure:

- `miniprogram/` — front-end pages and assets
- `cloudfunctions/` — cloud functions
- WXML + JavaScript/TypeScript + LESS
- pages include login/registration, quiz, prize, information, center, store, and other modules

The simulator is a separate static website. It must not connect to production CloudBase or expose participant-level data unless a later, separately reviewed backend is added.

## Product requirements for this simulator

1. Default to bilingual Chinese + English display.
2. Allow Chinese-only and English-only modes.
3. Keep observed data clearly separated from scenario assumptions.
4. Preserve the Monte Carlo uncertainty intervals.
5. Optimize for research completion and usable samples, not only clicks.
6. Make the project deployable as a public static site with GitHub Pages.
7. Never commit API keys, participant data, CloudBase exports, OpenIDs, raw survey responses, or private reports.
