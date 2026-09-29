# Awesome Uncensored AI Video Models

> A community-maintained catalog of current AI video-generation and video-editing models—including local weights, adapters, hosted endpoints, and APIs—with a focus on filtering, access, licensing, and practical trade-offs.

“Uncensored” is not a standardized technical term. A video model’s behavior can change with the checkpoint, text encoder, prompt wrapper, inference pipeline, UI, post-processing, provider policy, and model version. This list records those details instead of treating the label as a guarantee.

**Last reviewed:** 2026-09-29

## Related Projects

- [awesome-uncensored-llms](https://github.com/Anil-matcha/awesome-uncensored-llms) — Companion catalog for language models and LLM fine-tunes.
- [awesome-uncensored-ai-models](https://github.com/Anil-matcha/awesome-uncensored-ai-models) — Directory for all three uncensored model catalogs.
- [awesome-ai-video-models](https://github.com/Anil-matcha/awesome-ai-video-models) — Compare mainstream and open video models by provider, price, speed, and capability alongside this filtering-focused catalog.
- [awesome-uncensored-ai-image-models](https://github.com/Anil-matcha/awesome-uncensored-ai-image-models) — Companion catalog for image-generation and image-editing model variants.
- [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI) — Self-hosted image and video studio for testing generative-media workflows.
- [Generative-Media-Skills](https://github.com/SamurAIGPT/Generative-Media-Skills) — Run and automate media-generation experiments from an AI coding agent.

## Contents

- [Recent local candidates](#recent-local-candidates)
- [Hosted/API families](#hostedapi-families)
- [Filtered reference models](#filtered-reference-models)
- [Community-reported variants](#community-reported-variants)
- [Established local baselines](#established-local-baselines)
- [How entries are classified](#how-entries-are-classified)
- [What each entry should include](#what-each-entry-should-include)
- [Related catalogs and surveys](#related-catalogs-and-surveys)
- [Contributing](#contributing)
- [Responsible use](#responsible-use)

## Recent local candidates

These entries are included because weights, code, or a reproducible local pipeline are publicly available. Local execution removes a hosted moderation layer, but open weights alone do not prove that a model is uncensored or low-filter.

| Model / family | Release / update | Access | Video capabilities | Status | Official source |
| --- | --- | --- | --- | --- | --- |
| Wan2.2 | 2025-07 onward | Local weights | Text-to-video, image-to-video, text-image-to-video, speech-to-video, and character animation | Open-weight candidate | [Official repository](https://github.com/Wan-Video/Wan2.2) |
| Wan2.1 | 2025-02 onward | Local weights | Text-to-video, image-to-video, first/last-frame-to-video, and VACE video creation/editing | Open-weight candidate | [Official repository](https://github.com/Wan-Video/Wan2.1) |
| LTX-2 / LTX-2.3 | 2025-2026 | Local weights | Text-to-video, image-to-video, keyframes, LoRA control, and synchronized audio-video generation | Open-weight candidate; verify checkpoint terms | [Code repository](https://github.com/Lightricks/LTX-Video) · [LTX-2.3 model card](https://huggingface.co/Lightricks/LTX-2.3) |
| HunyuanVideo-1.5 | 2025-12 onward | Local weights | Text-to-video and image-to-video, including step-distilled inference variants | Open-weight candidate; review the custom terms | [Official repository](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5) |
| HunyuanVideo | 2024-12 | Local weights | Text-to-video with local inference and fine-tuning workflows | Open-weight candidate; review the custom terms | [Official repository](https://github.com/Tencent-Hunyuan/HunyuanVideo) |
| CogVideoX / CogVideoX1.5 | 2024-08 onward | Local weights | Text-to-video, image-to-video, and video continuation | Open-weight candidate; checkpoint terms vary | [Official repository](https://github.com/zai-org/CogVideo) |
| Open-Sora | 2024-2026 | Local weights and training code | Open video-generation research and production pipeline | Open-weight candidate; verify the selected release | [Official repository](https://github.com/hpcaitech/Open-Sora) |
| Allegro / Allegro-TI2V | 2024-12 onward | Local weights | Text-to-video and text/image-to-video research models | Open-weight candidate | [Official repository](https://github.com/rhymes-ai/Allegro) |
| Mochi 1 | 2024-10 | Local weights | Text-to-video with LoRA fine-tuning and ComfyUI workflows | Open-weight candidate | [Official repository](https://github.com/genmoai/mochi) |
| AnimateDiff | 2023-08 onward | Local modules and checkpoints | Animation of Stable Diffusion image models with motion modules | Open-weight candidate; base-model terms apply | [Official repository](https://github.com/guoyww/AnimateDiff) |
| Stable Video Diffusion | 2023-11 | Local weights | Image-to-video and video foundation-model research | To verify per checkpoint and license | [Model card](https://huggingface.co/stabilityai/stable-video-diffusion-img2vid-xt) |
| VideoCrafter2 | 2024 | Local weights and code | Text-to-video and image-to-video research models | To verify per checkpoint and license | [Official repository](https://github.com/AILab-CVC/VideoCrafter) |

### Why local access matters

Local inference can avoid provider-side prompt moderation, endpoint-specific refusals, and hosted output filters. It does not remove the model license, dataset restrictions, UI safeguards, watermarking, or legal obligations. The exact checkpoint and pipeline must be recorded for every claim.

## Hosted/API families

These newer Wan families are listed separately because the public model documentation exposes them as hosted/API model IDs rather than as local checkpoints in the official Wan2.1/Wan2.2 repositories. Their filtering status is endpoint-specific and must be tested against the exact provider, model ID, snapshot, region, and date.

| Model / family | Release / update | Access | Video capabilities | Status | Official source |
| --- | --- | --- | --- | --- | --- |
| Wan 2.7 | 2026 API snapshots | Hosted / API | T2V, I2V, R2V, video editing, audio sync, multi-shot narrative, reference images/videos, 720P/1080P, 2–15s | Community-reported endpoint; verify exact deployment | [Video-model documentation](https://docs.qwencloud.com/developer-guides/getting-started/video-models) |
| Wan 2.6 | 2025–2026 API snapshots | Hosted / API | T2V, I2V, R2V, audio sync, multi-shot narrative, 720P/1080P, 2–15s | Community-reported endpoint; verify exact deployment | [Video-model documentation](https://docs.qwencloud.com/developer-guides/getting-started/video-models) |
| Wan 2.5 | 2025 API previews | Hosted / API | T2V and I2V with audio sync, 480P/720P/1080P, 5–10s | Community-reported endpoint; verify exact deployment | [Video-model documentation](https://docs.qwencloud.com/developer-guides/getting-started/video-models) |
| Kling VIDEO 3.0 / VIDEO 3.0 Omni | 2026 | Hosted / API | Text-to-video, image-to-video, native audio, multi-shot storyboards, multimodal references, and cross-task workflows | Endpoint-specific; uncensored status to verify | [Official platform](https://kling.ai/) · [VIDEO 3.0 guide](https://app.klingai.com/cn/quickstart/klingai-video-3-model-user-guide) |
| Kling VIDEO 2.6 / VIDEO O1 | 2025–2026 | Hosted / API | T2V/I2V, start-and-end frames, native audio, and reference workflows; predecessor families to VIDEO 3.0 | Endpoint-specific; uncensored status to verify | [Official VIDEO 3.0 guide](https://app.klingai.com/cn/quickstart/klingai-video-3-model-user-guide) |
| Seedance 2.0 / 2.0 Fast | 2026 | Hosted / API | Text, image, audio, and video inputs with joint audio-video generation, reference control, editing, and extension | Endpoint-specific; uncensored status to verify | [Official model page](https://seed.bytedance.com/en/seedance2_0) · [ModelArk API docs](https://docs.byteplus.com/api/docs/ModelArk/2298881) |
| Seedance 1.5 Pro | 2025-12 | Hosted / API | Native synchronized audio-video generation, T2V/I2V, lip-sync, and cinematic camera control | Endpoint-specific; uncensored status to verify | [Official technical page](https://seed.bytedance.com/en/public_papers/seedance-1-5-pro-a-native-audio-visual-joint-generation-foundation-model) · [ModelArk API docs](https://docs.byteplus.com/api/docs/ModelArk/2298881) |
| Seedance 1.0 Pro / Pro Fast | 2025 | Hosted / API | Text-to-video, image-to-video, multi-shot generation, and prompt-controlled motion | Endpoint-specific; uncensored status to verify | [Official model page](https://seed.bytedance.com/en/seedance) · [ModelArk API docs](https://docs.byteplus.com/api/docs/ModelArk/2298881) |

## Filtered reference models

These hosted models are useful quality and capability references, but their provider policies and moderation layers make them poor fits for an uncensored catalog. They remain here so frontier quality is not confused with low filtering.

| Model / family | Access | Why it is a reference only | Official source |
| --- | --- | --- | --- |
| Sora | Hosted / API | Provider policy and hosted safety systems apply | [OpenAI Sora](https://openai.com/sora/) |
| Veo | Hosted / API | Google policy controls and hosted access apply | [Google DeepMind Veo](https://deepmind.google/models/veo/) |
| Runway video models | Hosted | Hosted moderation and platform terms apply | [Runway research](https://runwayml.com/research) |
| Kling video models | Hosted | Hosted moderation and platform terms apply | [Kling AI](https://klingai.com/) |
| Pika video models | Hosted | Hosted moderation and platform terms apply | [Pika](https://pika.art/) |

## Community-reported variants

The [dedicated variant matrix](UNCENSORED-MODELS.md) records full checkpoints, LoRAs, text encoders, quantizations, and community-reported endpoints whose creators or users describe them as uncensored, low-filter, or NSFW-capable.

The initial matrix includes community-labeled Wan and LTX derivatives found in public model repositories. These entries are not independent certifications: the exact base model, file revision, license, and inference setup still need to be checked before use.

## Established local baselines

These models remain useful reference points even when no uncensored claim is made.

### General-purpose video models

| Model | Access | Family | Filtering status | Source |
| --- | --- | --- | --- | --- |
| ModelScope Text-to-Video | Local weights | ModelScope / DAMO | To verify | [Model card](https://huggingface.co/damo-vilab/text-to-video-ms-1.7b) |
| VideoCrafter1 | Local weights | VideoCrafter | To verify | [Official repository](https://github.com/AILab-CVC/VideoCrafter) |
| I2VGen-XL | Local weights | Alibaba DAMO | To verify | [Model card](https://huggingface.co/ali-vilab/i2vgen-xl) |
| DynamiCrafter | Local weights | Image-to-video diffusion | To verify | [Official repository](https://github.com/Doubiiu/DynamiCrafter) |

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

These labels describe observed behavior and documentation quality. They do not grant permission to create, distribute, or use any particular content.

## What each entry should include

Every accepted entry should document:

- exact model, checkpoint, adapter, or text-encoder version;
- release date or most recent major update;
- official source, access method, and download/API links;
- whether it is local, hosted, API-only, or available in multiple forms;
- base architecture and intended video task: T2V, I2V, V2V, R2V, S2V, animation, or editing;
- supported resolution, frame rate, duration, audio behavior, and aspect ratios where known;
- license, commercial-use terms, provider terms, and restrictions;
- approximate VRAM, latency, offloading, quantization, or hardware requirements;
- supported inference tools and workflows;
- whether filtering is in the weights, text encoder, pipeline, UI, provider, post-processor, or an optional safety checker;
- reproducible notes about testing, including date, file revision, and setup.

## Related catalogs and surveys

These projects were checked while preparing this catalog. They cover adjacent scopes and are useful references, but none is a dedicated, source-tracked catalog of uncensored video models.

- [Awesome Video Generation](https://github.com/backblaze-labs/awesome-video-generation) — APIs, tools, infrastructure, and open models for developers.
- [Awesome Text-to-Video](https://github.com/jianzhnie/awesome-text-to-video) — model comparison tables and text-to-video resources.
- [Awesome Video Generation](https://github.com/kongzhecn/awesome-video-generation) — research papers and video-generation methods.
- [State of open video generation models in Diffusers](https://huggingface.co/blog/video_gen) — an open-model overview and Diffusers guidance.
- [Hugging Face video-generation models](https://huggingface.co/models?library=video-generation) — a live model index rather than a curated safety catalog.

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a model. Short version: cite primary sources, preserve license and provider terms, avoid vague “uncensored” claims, and keep entries factual and reproducible.

## Responsible use

Use these resources for lawful, consensual, and ethical creative or research work. Do not use them to create sexual content involving minors, non-consensual intimate imagery, targeted harassment, fraud, impersonation, or other abusive or illegal material. Do not submit real-person sexual examples or personal data to this repository. Follow the model license, provider terms, and the laws that apply to you.

## License

The original documentation and catalog content in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Individual models, providers, APIs, checkpoints, code, datasets, and linked resources remain subject to their own licenses and terms.
