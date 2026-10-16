# Awesome AI Models Catalog & Android App

> A community-maintained catalog and Android application of free publicly available AI models, LLMs, video-generation models, game-generation tools, and full-app AI generators.

**Last reviewed:** 2026-08-06

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
