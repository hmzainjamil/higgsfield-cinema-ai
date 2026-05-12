# Higgsfield Cinema AI — Automation Stack

> 29 cinematic camera movement prompts + full AI video production pipeline for Higgsfield Cinema Studio

[![Claude Code](https://img.shields.io/badge/Claude%20Code-Automation-blue?style=flat)](https://claude.ai/code)
[![Higgsfield](https://img.shields.io/badge/Higgsfield-Cinema%20Studio-purple?style=flat)](https://higgsfield.ai)
[![Nano Banana Pro](https://img.shields.io/badge/Model-Nano%20Banana%20Pro-orange?style=flat)](https://higgsfield.ai)

## What's Inside

| File | Purpose |
|---|---|
| `higgsfield-cinema-agent.md` | Full agent spec — all 29 shots, model routing, revenue tiers |
| `higgsfield-shot-generator` | Python CLI — generates adapted prompts for any subject |
| `SKILL.md` | Complete skill with all 29 prompt texts, formulas, use cases |
| `higgsfield-cinematic-workflow.json` | 7-step production workflow (brief → hero frame → Cinema Studio → edit) |

## Quick Start

```bash
# List all 29 shots
python3 higgsfield-shot-generator --list-shots

# Generate 8 commercial shots for your subject
python3 higgsfield-shot-generator "luxury car" --style commercial --shots 8

# Generate all 29 shots
python3 higgsfield-shot-generator "your subject" --all-shots

# Generate a 6-beat storyboard
python3 higgsfield-shot-generator "brand narrative" --storyboard --beats 6
```

## 29 Shot Categories

| Category | Shots | Emotion |
|---|---|---|
| Straight Line | dolly-in/out, rush, pan L/R, tilt up/down, dolly L/R, over-shoulder | Establish, reveal |
| Orbital/Crane | orbit-180, full-360, cinematic-arc, jib-up/down, crane-overhead | Character presence |
| Zoom | zoom-in/out, crash-zoom, rack-focus, fisheye | Intensity, focus shift |
| Aerial | drone-flyover, aerial-orbit, fpv-drone, aerial-pullback, macro | Scale, energy |
| Tracking | leading, following, side-tracking, pov-walk, through-shot | Journey, immersion |

## Model Routing

- **Hero frame** → Nano Banana Pro (2K)
- **Cinematic video** → Kling 2.6 (1080p, audio)
- **Character acting** → Google V3.1 (8s, audio)
- **Viral/candid** → Sora 2
- **Character consistency** → Higgsfield Soul 2 (22 styles)

## DigiMinds Revenue Tiers

| Package | Shots | Deliverable | Rate |
|---|---|---|---|
| Social Reel | 5 | 9:16 viral clip | $200-500 |
| Brand Intro | 10 | 30s commercial | $500-1500 |
| Full Commercial | 29 | 60-90s spot | $2000-5000 |
