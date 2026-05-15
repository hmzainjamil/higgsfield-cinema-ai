# higgsfield-cinema-ai
Higgsfield Cinema Studio automation — 29 shot types, storyboard generator, cinematic workflow for DigiMinds

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=flat&labelColor=555&logo=python)
![Higgsfield](https://img.shields.io/badge/Higgsfield-Cinema_Studio-black?style=flat&labelColor=555)
![Nano_Banana](https://img.shields.io/badge/Nano_Banana-Pro-yellow?style=flat&labelColor=555)
![Kling](https://img.shields.io/badge/Kling-2.6-purple?style=flat&labelColor=555)
![Google](https://img.shields.io/badge/Google-V3.1-4285F4?style=flat&labelColor=555)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat&labelColor=555)

[Concepts](#-concepts) · [How It Works](#️-how-it-works) · [Install](#-install) · [Shot Types](#-shot-types) · [Tips](#-tips-and-tricks-12) · [Startups](#️-startups--businesses)

---

## 🧠 CONCEPTS

| Feature | Location | Description |
|---------|----------|-------------|
| [**higgsfield-shot-generator**](higgsfield-shot-generator) | `~/.claude/bin/higgsfield-shot-generator` | CLI: generate 1–29 shots from subject + style in one command |
| [**29 Shot Categories**](higgsfield-shot-generator) | `--all-shots` | Straight line, orbital, zoom, aerial, tracking — full cinematic language |
| [**Storyboard Mode**](higgsfield-shot-generator) | `--storyboard --beats N` | Narrative storyboard with camera movement per story beat |
| [**Model Router**](higgsfield-shot-generator) | `--style commercial` | Auto-routes: hero frame→Nano Banana, video→Kling 2.6, dialogue→V3.1 |
| [**Soul 2 Styles**](higgsfield-shot-generator) | Higgsfield Soul 2 | 22 cinematic style presets for character consistency |
| [**DigiMinds Revenue**](higgsfield-shot-generator) | Agency pricing | $500 reel → $3,000 full commercial — 90% margin |

### 🔥 Hot

| Feature | Location | Description |
|---------|----------|-------------|
| [**One-prompt → 8 shots**](higgsfield-shot-generator) | `python3 higgsfield-shot-generator "subject" --shots 8` | Full shot list with prompts + model assignment in seconds |
| [**Nano Banana 2K**](higgsfield-shot-generator) | Hero frame generation | 2K resolution, 9x16/16x9, best-in-class still quality |
| [**Audio-enabled video**](higgsfield-shot-generator) | Kling 2.6 + V3.1 | Both support native audio — dialogue, SFX, music in output |

---

## ⚙️ HOW IT WORKS

```
python3 higgsfield-shot-generator "luxury car reveal" --style commercial --shots 8
         ↓
Model Router assigns each shot:
  ├── Hero frame (still) → Nano Banana Pro (2K)
  ├── Cinematic video    → Kling 2.6 (1080p, 10s, audio)
  ├── Character acting   → Google V3.1 (1080p, 8s, audio)
  └── Aerial/drone       → Sora 2
         ↓
Storyboard JSON → shot prompts → API calls
         ↓
Output: ~/Downloads/higgsfield-output/[session]/
```

**Soul 2 style presets:** cinematic-noir · golden-hour · neon-city · documentary · fashion-editorial · (22 total)

---

## 🚀 INSTALL

```bash
git clone https://github.com/hmzainjamil/higgsfield-cinema-ai
cd higgsfield-cinema-ai
cp higgsfield-shot-generator ~/.claude/bin/
chmod +x ~/.claude/bin/higgsfield-shot-generator
mkdir -p ~/Downloads/higgsfield-output
```

---

## 🎬 SHOT TYPES

| Category | Shots | Best For |
|---|---|---|
| **Straight line** | dolly-in, dolly-out, pan-left, pan-right, tilt-up, tilt-down, rush, over-shoulder | Establishing, environment reveal |
| **Orbital/Crane** | orbit-180, full-360, cinematic-arc, jib-up, jib-down, overhead-top | Character intro, emotional weight |
| **Zoom** | zoom-in, zoom-out, crash-zoom, rack-focus, fisheye-warp | Intensity, attention shift |
| **Aerial** | drone-flyover, aerial-orbit, fpv-drone, aerial-pullback, macro-detail | Scale, context, raw energy |
| **Tracking** | leading-track, following-track, side-tracking, pov-walk, through-shot | Journey, immersion, POV |

---

## 📟 COMMANDS

| Command | Description |
|---------|-------------|
| `python3 higgsfield-shot-generator "subject"` | Generate 5 default shots |
| `--shots N` | Generate N shots |
| `--style commercial\|cinematic\|documentary\|fashion` | Style preset |
| `--all-shots` | All 29 shot types with prompts |
| `--storyboard --beats 6` | 6-beat narrative storyboard |
| `--shot "dolly-in" "subject"` | Single specific shot |
| `--list-shots` | List all 29 shot names |

---

## 💡 TIPS AND TRICKS (12)

[shots](#tips-shots) · [models](#tips-models) · [agency](#tips-agency) · [production](#tips-production)

<a id="tips-shots"></a>■ **Shot Selection (3)**

| Tip | Source |
|-----|--------|
| Orbit-180 for character intro — creates instant emotional investment, used in every major film | [HMZ](https://github.com/hmzainjamil) |
| Crash-zoom for tension — fast zoom-in on face at reveal moment, 3x engagement on social | [DigiMinds](https://github.com/hmzainjamil) |
| Leading-track for products — camera leads subject into frame, feels premium and intentional | [HMZ](https://github.com/hmzainjamil) |

<a id="tips-models"></a>■ **Model Routing (3)**

| Tip | Source |
|-----|--------|
| Nano Banana Pro for hero frames — 2K still quality unmatched for product reveals | [HMZ](https://github.com/hmzainjamil) |
| Kling 2.6 for action/motion shots — 10s clips with audio, best temporal consistency | [DigiMinds](https://github.com/hmzainjamil) |
| V3.1 for dialogue/talking head — native audio sync makes it best for spokesperson ads | [HMZ](https://github.com/hmzainjamil) |

<a id="tips-agency"></a>■ **Agency Pricing (3)**

| Tip | Source |
|-----|--------|
| 30s commercial reel (8 shots): quote $500–800. Takes 20min with this tool. 95% margin | [DigiMinds](https://github.com/hmzainjamil) |
| Full commercial package (29 shots + storyboard): $2,500–4,000. Deliver in 2hrs | [HMZ](https://github.com/hmzainjamil) |
| Retainer: $1,200/mo for 4 reels/month = 4hrs work = $300/hr effective rate | [DigiMinds](https://github.com/hmzainjamil) |

<a id="tips-production"></a>■ **Production (3)**

| Tip | Source |
|-----|--------|
| Run `--storyboard --beats 6` first — share with client for approval before rendering | [HMZ](https://github.com/hmzainjamil) |
| Soul 2 `cinematic-arc` style + rack-focus = instant premium feel for any product | [DigiMinds](https://github.com/hmzainjamil) |
| Batch all shots in one call — parallel API requests, 8 shots = same time as 1 | [HMZ](https://github.com/hmzainjamil) |

---

## ☠️ STARTUPS / BUSINESSES

| This Repo / Feature | Replaced |
|-|-|
| **higgsfield-shot-generator** | [Runway Gen-3](https://runwayml.com), [Pika Labs](https://pika.art), [Luma Dream Machine](https://lumalabs.ai) |
| **Storyboard generator** | [FrameForge](https://frameforge.com), [Boords](https://boords.com), [StudioBinder](https://studiobinder.com) |
| **Model router (auto-assign)** | [Replicate](https://replicate.com), [fal.ai](https://fal.ai) — manual model selection |
| **DigiMinds commercial pipeline** | [Arcads](https://arcads.ai), [HeyGen](https://heygen.com), [Synthesia](https://synthesia.io) |
| **Soul 2 style consistency** | [Midjourney](https://midjourney.com), [Adobe Firefly](https://firefly.adobe.com) style reference |

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=hmzainjamil/higgsfield-cinema-ai&type=Date)](https://star-history.com/#hmzainjamil/higgsfield-cinema-ai&Date)

---

<div align="center">
Built by <a href="https://github.com/hmzainjamil">HMZ</a> · <a href="https://digiminds.org">DigiMinds</a> · AI cinematic production pipeline
</div>
