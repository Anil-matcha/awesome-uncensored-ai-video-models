# Awesome AI Models Catalog & Android App

> A community-maintained catalog and Android application of free publicly available AI models, LLMs, video-generation models, game-generation tools, and full-app AI generators.

**Last reviewed:** 2026-09-29

## Android Application (APK & AAB)

This repository includes a native Android app built with **Gradle** and **Jetpack Compose** that lets users search, filter, and access all free AI providers, LLM endpoints, video generation models, and full-app / game generators.

### Building the Android App

To build the debug and release APKs and Android App Bundles (AAB) using Gradle:

```bash
# Build Debug APK & AAB
./gradlew assembleDebug bundleDebug

# Build Release APK & AAB
./gradlew assembleRelease bundleRelease
```
| Model / family | Release / update | Access | Video capabilities | Status | Model link |
| --- | --- | --- | --- | --- | --- |
| Wan2.2 | 2025-07 onward | Local weights | Text-to-video, image-to-video, text-image-to-video, speech-to-video, and character animation | Open-weight candidate | [Wan 2.2 T2V](https://muapi.ai/playground/wan2.2-text-to-video) · [I2V](https://muapi.ai/playground/wan2.2-image-to-video) · [Wan 2.2 Spicy I2V](https://muapi.ai/playground/wan2.2-spicy-image-to-video) · [Spicy Video Extend](https://muapi.ai/playground/wan2.2-spicy-video-extend) |
| Wan2.1 | 2025-02 onward | Local weights | Text-to-video, image-to-video, first/last-frame-to-video, and VACE video creation/editing | Open-weight candidate | [Wan 2.1 T2V](https://muapi.ai/playground/wan2.1-text-to-video) · [I2V](https://muapi.ai/playground/wan2.1-image-to-video) |
| LTX-2 / LTX-2.3 | 2025-2026 | Local weights | Text-to-video, image-to-video, keyframes, LoRA control, and synchronized audio-video generation | Open-weight candidate; verify checkpoint terms | [LTX-2.3 T2V](https://muapi.ai/playground/ltx-2.3-text-to-video) · [I2V](https://muapi.ai/playground/ltx-2.3-image-to-video) |
| HunyuanVideo | 2024-12 | Local weights | Text-to-video with local inference and fine-tuning workflows | Open-weight candidate; review the custom terms | [HunyuanVideo T2V](https://muapi.ai/playground/hunyuan-text-to-video) · [I2V](https://muapi.ai/playground/hunyuan-image-to-video) |

The compiled artifacts will be placed in:
- **APK**: `app/build/outputs/apk/debug/app-debug.apk` and `app/build/outputs/apk/release/app-release.apk`
- **AAB**: `app/build/outputs/bundle/debug/app-debug.aab` and `app/build/outputs/bundle/release/app-release.aab`

---

## Contents

- [Free LLM Providers & Public Endpoints](#free-llm-providers--public-endpoints)
- [Video Generation Models](#video-generation-models)
- [Game & Full-App AI Generators](#game--full-app-ai-generators)
- [Uncensored & Low-Filter Video Models](#uncensored--low-filter-video-models)
- [Related Projects](#related-projects)
- [Contributing](#contributing)

---
| Model / family | Release / update | Access | Video capabilities | Status | Model link |
| --- | --- | --- | --- | --- | --- |
| Wan 2.7 | 2026 API snapshots | Hosted / API | T2V, I2V, R2V, video editing, audio sync, multi-shot narrative, reference images/videos, 720P/1080P, 2–15s | Community-reported endpoint; verify exact deployment | [Wan 2.7 Spicy](https://muapi.ai/wan-spicy) · [I2V](https://muapi.ai/playground/wan2.7-image-to-video-spicy) |
| Wan 2.6 | 2025–2026 API snapshots | Hosted / API | T2V, I2V, R2V, audio sync, multi-shot narrative, 720P/1080P, 2–15s | Community-reported endpoint; verify exact deployment | [Wan 2.6 Spicy I2V](https://muapi.ai/playground/wan2.6-image-to-video-spicy) |
| Wan 2.5 | 2025 API previews | Hosted / API | T2V and I2V with audio sync, 480P/720P/1080P, 5–10s | Community-reported endpoint; verify exact deployment | [Wan 2.5 T2V](https://muapi.ai/playground/wan2.5-text-to-video) · [I2V](https://muapi.ai/playground/wan2.5-image-to-video) |
| Kling VIDEO 3.0 / VIDEO 3.0 Omni | 2026 | Hosted / API | Text-to-video, image-to-video, native audio, multi-shot storyboards, multimodal references, and cross-task workflows | Endpoint-specific; uncensored status to verify | [Kling 3.0 T2V](https://muapi.ai/playground/kling-v3.0-pro-text-to-video) · [I2V](https://muapi.ai/playground/kling-v3.0-pro-image-to-video) · [Kling 3.0 Omni](https://muapi.ai/playground/kling-v3.0-omni-pro-text-to-video) |
| Kling VIDEO 2.6 / VIDEO O1 | 2025–2026 | Hosted / API | T2V/I2V, start-and-end frames, native audio, and reference workflows; predecessor families to VIDEO 3.0 | Endpoint-specific; uncensored status to verify | [Kling 2.6 T2V](https://muapi.ai/playground/kling-v2.6-pro-t2v) · [Kling O1](https://muapi.ai/playground/kling-o1-text-to-video) |
| Seedance 2.0 / 2.0 Fast | 2026 | Hosted / API | Text, image, audio, and video inputs with joint audio-video generation, reference control, editing, and extension | Endpoint-specific; uncensored status to verify | [Seedance 2.0 Spicy T2V](https://muapi.ai/playground/seedance-2-spicy-text-to-video) · [I2V](https://muapi.ai/playground/seedance-2-spicy-image-to-video) · [Fast T2V](https://muapi.ai/playground/seedance-2-spicy-text-to-video-fast) · [Fast I2V](https://muapi.ai/playground/seedance-2-spicy-image-to-video-fast) · [Omni Reference](https://muapi.ai/playground/seedance-2-spicy-omni-reference) |
| Wan 3.0 | 2026 | Hosted / API | T2V, I2V, and R2V, including spicy variants | Community-reported endpoint; verify exact deployment | [Wan 3.0](https://muapi.ai/wan-3) · [T2V](https://muapi.ai/playground/wan3.0-text-to-video) · [I2V](https://muapi.ai/playground/wan3.0-image-to-video) · [Wan 3.0 Spicy T2V](https://muapi.ai/playground/wan3.0-spicy-text-to-video) · [Spicy I2V](https://muapi.ai/playground/wan3.0-spicy-image-to-video) · [Spicy R2V](https://muapi.ai/playground/wan3.0-spicy-reference-to-video) |
| Seedance 2.5 | 2026 | Hosted / API | T2V and I2V up to 4K, including spicy variants | Community-reported endpoint; verify exact deployment | [Seedance 2.5](https://muapi.ai/seedance-2.5) · [T2V](https://muapi.ai/playground/seedance-2.5-text-to-video) · [I2V](https://muapi.ai/playground/seedance-2.5-image-to-video) · [Seedance 2.5 Spicy](https://muapi.ai/seedance-2.5-spicy) · [Spicy T2V](https://muapi.ai/playground/seedance-2.5-spicy-text-to-video) · [Spicy I2V](https://muapi.ai/playground/seedance-2.5-spicy-image-to-video) · [Spicy First-Last Frame](https://muapi.ai/playground/seedance-2.5-spicy-first-last-frame) · [Spicy Omni Reference](https://muapi.ai/playground/seedance-2.5-spicy-omni-reference) · [Spicy Video Edit](https://muapi.ai/playground/seedance-2.5-spicy-video-edit) · [Spicy Video Extend](https://muapi.ai/playground/seedance-2.5-spicy-video-extend) · [Spicy Motion Control](https://muapi.ai/playground/seedance-2.5-spicy-motion-control) |
| MiniMax Hailuo H3 | 2026 | Hosted / API | Text-to-video and image-to-video, including a spicy I2V variant | Community-reported endpoint; verify exact deployment | [Hailuo H3 Spicy](https://muapi.ai/minimax-h3-spicy) · [Spicy I2V](https://muapi.ai/playground/minimax-h3-image-to-video-spicy) · [H3 T2V](https://muapi.ai/playground/minimax-h3-text-to-video) · [I2V](https://muapi.ai/playground/minimax-h3-image-to-video) |
| Seedance 2.0 Spicy / Fast / Mini | 2026 | Hosted / API | T2V, I2V, and omni-reference, with Fast and Mini tiers | Community-reported endpoint; verify exact deployment | [Seedance 2.0 Spicy T2V](https://muapi.ai/playground/seedance-2-spicy-text-to-video) · [I2V](https://muapi.ai/playground/seedance-2-spicy-image-to-video) · [Mini T2V](https://muapi.ai/playground/seedance-2-mini-spicy-text-to-video) · [Mini I2V](https://muapi.ai/playground/seedance-2-mini-spicy-image-to-video) · [Mini Omni Reference](https://muapi.ai/playground/seedance-2-mini-spicy-omni-reference) |
| Seedance 1.5 Pro | 2025-12 | Hosted / API | Native synchronized audio-video generation, T2V/I2V, lip-sync, and cinematic camera control | Endpoint-specific; uncensored status to verify | [Seedance 1.5 Pro T2V](https://muapi.ai/playground/seedance-v1.5-pro-t2v) · [I2V](https://muapi.ai/playground/seedance-v1.5-pro-i2v) |
| Seedance 1.0 Pro / Pro Fast | 2025 | Hosted / API | Text-to-video, image-to-video, multi-shot generation, and prompt-controlled motion | Endpoint-specific; uncensored status to verify | [Seedance 1.0 Pro T2V](https://muapi.ai/playground/seedance-pro-t2v) · [I2V](https://muapi.ai/playground/seedance-pro-i2v) |

## Free LLM Providers & Public Endpoints

Free, zero-cost API providers, endpoints, and local execution runners for LLMs:

| Provider / Platform | Access / Model Options | Key Capabilities & Limits | Official Link |
| --- | --- | --- | --- |
| **Google AI Studio** | Gemini 1.5 Pro, Gemini 1.5 Flash | Free API tier with high rate limits, up to 2M token context window, multimodal vision/audio input. | [AI Studio](https://aistudio.google.com/) |
| **Groq LPU** | Llama 3.3 70B, DeepSeek R1 Distill, Gemma 2, Whisper | Ultra-fast LPU inference API with free tier rate limits. | [Groq Console](https://console.groq.com/) |
| **Hugging Face** | Thousands of open-source LLMs & Embeddings | Free Serverless Inference API for open-weight models on Hugging Face Hub. | [HF Serverless API](https://huggingface.co/docs/api-inference/) |
| **OpenRouter** | DeepSeek R1, Llama 3.3, Qwen 2.5, Mistral | Unified API gateway offering public zero-cost open model endpoints. | [OpenRouter Free Models](https://openrouter.ai/models?max_price=0) |
| **Together AI** | Llama 3, Qwen 2.5, DeepSeek | Fast API endpoint with free initial credit pool for open models. | [Together AI](https://www.together.ai/) |
| **Ollama / LM Studio** | Local open weights (GGUF, Safetensors) | Run open LLMs locally on GPU/CPU with complete privacy and zero API fees. | [Ollama](https://ollama.com/) |
| Model / family | Access | Why it is a reference only | Model link |
| --- | --- | --- | --- |
| Sora | Hosted / API | Provider policy and hosted safety systems apply | [Sora 2](https://muapi.ai/playground/openai-sora-2-text-to-video) |
| Veo | Hosted / API | Google policy controls and hosted access apply | [Veo 3.1](https://muapi.ai/playground/veo3.1-text-to-video) · [Veo 4](https://muapi.ai/playground/veo-4-text-to-video) |
| Runway video models | Hosted | Hosted moderation and platform terms apply | [Runway](https://muapi.ai/playground/runway-text-to-video) |
| Kling video models | Hosted | Hosted moderation and platform terms apply | [Kling 3.0](https://muapi.ai/playground/kling-v3.0-pro-text-to-video) · [Kling 2.6](https://muapi.ai/playground/kling-v2.6-pro-t2v) |

## Community-reported variants

The [dedicated variant matrix](UNCENSORED-MODELS.md) records full checkpoints, LoRAs, text encoders, quantizations, and community-reported endpoints whose creators or users describe them as uncensored, low-filter, or NSFW-capable.

---

## Video Generation Models

Open-weight and public video-generation foundation models and pipelines:

| Model / Family | Access | Video Capabilities | Official Source |
| --- | --- | --- | --- |
| **Wan2.2 / Wan2.1** | Local weights & Hosted API | Text-to-video, image-to-video, speech-to-video, and character animation. | [Wan-Video Repo](https://github.com/Wan-Video/Wan2.2) |
| **LTX-2 / LTX-2.3** | Local weights | Real-time text-to-video, keyframing, LoRA control, synchronized audio. | [LTX-Video Repo](https://github.com/Lightricks/LTX-Video) |
| **HunyuanVideo / 1.5** | Local weights | High-resolution text-to-video and image-to-video with step distillation. | [HunyuanVideo Repo](https://github.com/Tencent-Hunyuan/HunyuanVideo) |
| **CogVideoX / 1.5** | Local weights | Text-to-video, image-to-video, and video extension workflows. | [CogVideo Repo](https://github.com/THUDM/CogVideo) |
| **Mochi 1** | Local weights | Open text-to-video model focused on motion dynamics and visual motion clarity. | [Mochi Repo](https://github.com/genmoai/mochi) |
| **AnimateDiff** | Local modules | Motion modules for animating Stable Diffusion image checkpoints. | [AnimateDiff Repo](https://github.com/guoyww/AnimateDiff) |
### Community tools and workflows

| Tool | Use | Source |
| --- | --- | --- |
| Diffusers video pipelines | Reproducible Python inference and model loading | [Hugging Face Diffusers](https://huggingface.co/docs/diffusers/main/en/using-diffusers/text-img2vid) |
| ComfyUI | Local node-based workflows and model integration | [ComfyUI](https://github.com/comfyanonymous/ComfyUI) |
| WanVideoWrapper | Alternative Wan workflows and optimizations for ComfyUI | [GitHub repository](https://github.com/kijai/ComfyUI-WanVideoWrapper) |

Want to add a model? Use the [submission template](.github/ISSUE_TEMPLATE/model-submission.md) or open a pull request.

## How entries are classified

- **Verified low-filter** — the exact checkpoint and inference setup are documented, and a maintainer has reproduced the reported behavior.
- **Creator-labeled** — the model card explicitly describes a low-filter, uncensored, or NSFW modification, but this repository has not independently reproduced it.
- **Community-labeled** — the repository name, tags, or surrounding metadata make the claim, but the card does not provide enough reproducible detail.
- **Community-reported endpoint** — users report behavior for a specific hosted provider, model snapshot, region, UI, or date; the claim must not be generalized to the whole model family.
- **Open-weight candidate** — the weights can be run or customized locally, but open weights are not proof that a model is uncensored.
- **Provider-filtered** — hosted access is governed by a provider’s content policy and safety systems.
- **To verify** — the model is a useful catalog candidate, but its filtering behavior, lineage, or licensing still needs documentation.
- **Removed** — the source is unavailable, the license is unclear, or the entry repeatedly fails the contribution requirements.

---

## Game & Full-App AI Generators

Publicly accessible web tools, studios, and frameworks for prompt-driven game and full-application creation:

| Tool / Platform | Category | Output & Capabilities | Link / Access |
| --- | --- | --- | --- |
| **v0 by Vercel** | Generative UI & Full App | Generates React, Next.js, and Tailwind CSS web components and apps from prompt descriptions. | [v0.dev](https://v0.dev/) |
| **Bolt.new** | Full-Stack Web App Studio | In-browser WebContainer VM that creates full-stack applications, installs NPM packages, and executes code. | [Bolt.new](https://bolt.new/) |
| **Lovable.dev** | Full-Stack Web App Studio | Natural language prompt to full-stack React & Supabase web application generator with GitHub integration. | [Lovable.dev](https://lovable.dev/) |
| **Claude Artifacts** | Interactive App Workspace | Interactive sandbox inside Claude for building single-page apps, HTML5 games, interactive tools, and visual widgets. | [Claude AI](https://claude.ai/) |
| **Rosebud AI Game Crafter** | 2D & 3D Web Game Generator | Creates browser games using Phaser.js or Three.js from prompt descriptions with code and asset editing. | [Rosebud AI](https://play.rosebud.ai/) |
| **Open-Generative-AI** | Self-Hosted Studio Framework | Open-source generative media studio for testing image, video, and interactive game generation workflows. | [Open-Generative-AI Repo](https://github.com/Anil-matcha/Open-Generative-AI) |

---

## Uncensored & Low-Filter Video Models

Detailed source-tracked list of local video checkpoints and community variants is maintained in [UNCENSORED-MODELS.md](UNCENSORED-MODELS.md).

---

## Related Projects

- [awesome-ai-video-models](https://github.com/Anil-matcha/awesome-ai-video-models) — Compare mainstream and open video models by provider, price, speed, and capability.
- [awesome-uncensored-ai-image-models](https://github.com/Anil-matcha/awesome-uncensored-ai-image-models) — Companion catalog for image-generation and image-editing model variants.
- [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI) — Self-hosted image, video, and app generation studio.

---

## License

The documentation and catalog content in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Code files and Android project source code are licensed under Apache-2.0.
