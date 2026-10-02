# Higgsfield Cinema Prompt Pack

A collection of cinematic shot prompts, a small Python prompt-output helper, and a JSON workflow concept. The repository does not contain a Higgsfield client, image or video generation API integration, provider router, install package, or application service.

## What is included

| Path | Purpose | Status |
|---|---|---|
| `SKILL.md` | Shot prompt library and image/video prompt formulas | Prompt documentation; its heading says 29 prompts, while the file contains entries numbered 1–31 |
| `higgsfield-cinema-agent.md` | Agent role and production guidance | Reference text; product, model, pricing, and capability statements are not verified by this repository |
| `higgsfield-cinematic-workflow.json` | Proposed creative workflow, model labels, output plan, and example commands | Design data only; no workflow runner or connected provider is included |
| `higgsfield-shot-generator` | Python script for adapting stored shot prompts and saving Markdown output | Local helper; has filesystem and optional subprocess effects described below |

## Prompt helper

The script uses only Python standard-library imports in the checked-in source. From the repository root, its source documents these forms:

```bash
python3 higgsfield-shot-generator --list-shots
python3 higgsfield-shot-generator --shot dolly-in "your subject"
python3 higgsfield-shot-generator "your subject" --style commercial --shots 6
python3 higgsfield-shot-generator "your subject" --all-shots
python3 higgsfield-shot-generator "your narrative" --storyboard --beats 6
```

These commands are documented from source and have not been run here. The helper is not an image or video renderer. Normal shot selection adapts stored prompt text and writes a Markdown file; storyboard mode calls an external local helper.

## Local data and side effects

At startup, the script reads `~/.claude/tier0.env` if present, imports its exported assignments into the process environment, and creates `~/.claude/tcc-logs` and `~/Downloads/higgsfield-output`. It writes generated Markdown under the latter directory.

Storyboard mode invokes `~/.claude/bin/llm-burst` with the storyboard prompt and a default model label of `groq,gemini`. This repository does not include that executable or establish which services it contacts. Review the executable, its configuration, and data destination before using it with private material. No credentials belong in this repository.

## Scope and limitations

- The JSON file describes a proposed sequence; it does not execute the listed stages or prove compatibility with named products or models.
- Model names, current capabilities, availability, prices, and revenue estimates in the prompt and agent materials are unverified here.
- No dependency manifest, test suite, license file, or release process is present in the repository tree reviewed for this guide.
- The GitHub repository metadata reports no declared license. Do not infer permission to reuse or redistribute the materials.

## Documentation map

- Start here for repository scope, source-backed commands, and local side effects.
- See [`SKILL.md`](SKILL.md) for the prompt library.
- See [`higgsfield-cinema-agent.md`](higgsfield-cinema-agent.md) for agent reference material.
- See [`higgsfield-cinematic-workflow.json`](higgsfield-cinematic-workflow.json) for the workflow concept.
- See [`higgsfield-shot-generator`](higgsfield-shot-generator) for the helper implementation.

## Maintainer

[hmzainjamil](https://github.com/hmzainjamil)
