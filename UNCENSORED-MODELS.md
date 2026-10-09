# Uncensored / Low-Filter Video Models

> A source-tracked list of local video checkpoints, LoRAs, text encoders, quantizations, and community-reported hosted endpoints whose creators or users describe them as uncensored, low-filter, or NSFW-capable.

**Last reviewed:** 2026-08-06

## Read this first

“Uncensored” is a claim about behavior, not a standardized model property. It may mean that a text encoder no longer refuses prompts, that a checkpoint was fine-tuned on adult imagery, that a pipeline safety checker was removed, or that a hosted endpoint uses a different moderation policy. These are different things.

This page records upstream claims and available metadata. It does not independently certify output behavior, provenance, legality, or safety. Do not infer commercial permission from the availability of weights. Video checkpoints also inherit requirements from their base model, VAE, text encoder, adapter, and inference code.

For hosted/API entries, the provider, region, model snapshot, endpoint, UI, and test date are part of the claim. Another endpoint using the same family name may behave differently.

## Evidence levels

- **Verified low-filter** — this repository reproduced the behavior for the exact checkpoint and setup.
- **Creator-labeled** — the model card explicitly describes the modification or intended content domain.
- **Community-labeled** — the repository name, tags, or surrounding metadata make the claim, but the card lacks reproducible detail.
- **Adapter** — this is a LoRA, text encoder, or other component and must be combined with its stated base model.
- **Community-reported endpoint** — users report behavior for a particular hosted provider or API, but this repository has not independently reproduced it.
- **Needs review** — the source is discoverable, but lineage, license, or behavior is not documented well enough for a stronger classification.

## Official open-weight families included as candidates

These entries are included because the weights or a local inference implementation are public. “Open-weight” describes access and customization, not a guarantee of unrestricted behavior.

| Model / family | Type | Base / requirement | Evidence | License and notes | Source |
| --- | --- | --- | --- | --- | --- |
| Wan2.1 local family | Video checkpoints | T2V-14B, I2V-14B-720P, I2V-14B-480P, T2V-1.3B, FLF2V-14B, VACE-1.3B, VACE-14B | Open-weight candidate | Official repository states Apache-2.0; review the exact checkpoint and dependencies. | [Official repository](https://github.com/Wan-Video/Wan2.1) |
| Wan2.2 local family | Video checkpoints | T2V-A14B, I2V-A14B, TI2V-5B, S2V-14B, Animate-14B | Open-weight candidate | Official repository states Apache-2.0; review the exact checkpoint and dependencies. | [Official repository](https://github.com/Wan-Video/Wan2.2) |
| LTX-2 / LTX-2.3 | Audio-video foundation model | LTX-2 pipeline and its checkpoint-specific terms | Open-weight candidate | Code is Apache-2.0; model-card and release terms still govern the selected weights. | [Code repository](https://github.com/Lightricks/LTX-Video) · [LTX-2.3 model card](https://huggingface.co/Lightricks/LTX-2.3) |
| HunyuanVideo-1.5 | Video checkpoint family | Official HunyuanVideo-1.5 code and checkpoint | Open-weight candidate | The repository uses custom terms; read the official license before redistribution or commercial use. | [Official repository](https://github.com/Tencent-Hunyuan/HunyuanVideo-1.5) |
| HunyuanVideo | Video checkpoint | Official HunyuanVideo code and checkpoint | Open-weight candidate | The repository uses custom terms; read the official license before redistribution or commercial use. | [Official repository](https://github.com/Tencent-Hunyuan/HunyuanVideo) |

## Community-labeled local variants

These repositories use an uncensored/NSFW label or describe a low-filter modification. They are listed as claims to investigate, not as independent certifications.

| Model / variant | Type | Base / requirement | Evidence | License and notes | Source |
| --- | --- | --- | --- | --- | --- |
| NSFW Wan 1.3B T2V | Full checkpoint | `Wan-AI/Wan2.1-T2V-1.3B` | Creator-labeled | Hugging Face metadata lists CreativeML OpenRAIL-M; the card also contains informal licensing language, so read the full terms and treat redistribution rights as unresolved until verified. | [Model card](https://huggingface.co/Cedbane96/NSFW_Wan_1.3b) |
| `ltxvideo-2b-nsfw` | Full checkpoint | LTX-Video 2B image-to-video pipeline | Community-labeled | The model page is marked sensitive and provides a Diffusers loading example; no clear license is shown on the page reviewed. | [Model card](https://huggingface.co/Muinez/ltxvideo-2b-nsfw) |
| `PinkCherry_NSFW_LTX23` | GGUF checkpoint / quantization | LTX-2.3 / LTX video stack | Community-labeled | The model page shows Apache-2.0, but lineage, training data, and output behavior require separate review. | [Model card](https://huggingface.co/SexGod1979/PinkCherry_NSFW_LTX23) |
| `WAN2.2_LoraSet_NSFW` | LoRA set | Wan2.2 | Adapter; community-labeled | The model page shows an unknown license. Confirm base-model compatibility and permissions before use. | [Model card](https://huggingface.co/lkzd7/WAN2.2_LoraSet_NSFW) |
| `WAN2.2_Lora_NSFW` | LoRA | Wan2.2 | Adapter; community-labeled | The name identifies a Wan2.2 LoRA, but the card, license, and training provenance must be checked before acceptance. | [Model card](https://huggingface.co/erikaoficialm/WAN2.2_Lora_NSFW) |
| `wan2.2_14b_i2v_480p_lightning_nsfw_diffusers` | Diffusers checkpoint / adapter candidate | Wan2.2 I2V 14B 480P | Community-labeled | The public model index exposes the name and I2V task; license, lineage, and behavior need review. | [Model card](https://huggingface.co/fdk6566/wan2.2_14b_i2v_480p_lightning_nsfw_diffusers) |
| `NSFW-Wan-UMT5-XXL` | Text-encoder candidate | Wan pipeline using UMT5-XXL | Needs review | The repository has no model card and no visible license on the page reviewed. It must not be treated as a verified replacement text encoder. | [Model card](https://huggingface.co/NSFW-API/NSFW-Wan-UMT5-XXL) |

## Community-reported hosted/API variants

Hosted reports are intentionally kept separate from local checkpoints. A submission must identify the exact provider, API model ID, version or snapshot, region, UI, test date, and provider terms. A model family’s local behavior cannot be inferred from a hosted endpoint, and a hosted endpoint’s behavior cannot be generalized to every deployment of that family.

The official API documentation identifies the following Wan families and model IDs. It documents their capabilities and output limits, but does not independently certify uncensored behavior; the low-filter claim remains endpoint-specific and requires reproduction.

| Model / variant family | Access | Model IDs / capability | Evidence | License and notes | Source |
| --- | --- | --- | --- | --- | --- |
| Wan 2.7 | Hosted / API | `wan2.7-t2v`, `wan2.7-t2v-2026-06-12`, `wan2.7-i2v`, `wan2.7-i2v-2026-04-25`, `wan2.7-r2v-2026-06-12`, `wan2.7-videoedit`; T2V, I2V, R2V, editing, audio, 720P/1080P, 2–15s | Needs review; community-reported endpoint status | Hosted terms apply. Record the exact provider, endpoint, snapshot, region, UI, and date tested. | [Video-model documentation](https://docs.qwencloud.com/developer-guides/getting-started/video-models) |
| Wan 2.6 | Hosted / API | `wan2.6-t2v`, `wan2.6-i2v`, `wan2.6-i2v-flash`, `wan2.6-r2v`, `wan2.6-r2v-flash`; T2V, I2V, R2V, audio, 720P/1080P, 2–15s | Needs review; community-reported endpoint status | Hosted terms apply. Do not infer behavior from local Wan2.1 or Wan2.2 weights. | [Video-model documentation](https://docs.qwencloud.com/developer-guides/getting-started/video-models) |
| Wan 2.5 | Hosted / API | `wan2.5-t2v-preview`, `wan2.5-i2v-preview`; T2V and I2V with audio sync, 480P/720P/1080P, 5–10s | Needs review; community-reported endpoint status | Hosted terms apply. The preview model IDs and endpoint policy must be recorded for any uncensored claim. | [Video-model documentation](https://docs.qwencloud.com/developer-guides/getting-started/video-models) |
| Kling VIDEO 3.0 / VIDEO 3.0 Omni | Hosted / API | Current Kling 3.0 video families; T2V, I2V, native audio, multi-shot, multimodal references, and cross-task workflows | Needs review; community-reported endpoint status | Hosted terms apply. The official platform describes the family, but uncensored behavior must be tied to an exact endpoint and test date. | [Official platform](https://kling.ai/) · [VIDEO 3.0 guide](https://app.klingai.com/cn/quickstart/klingai-video-3-model-user-guide) |
| Kling VIDEO 2.6 / VIDEO O1 | Hosted / API | Predecessor Kling families with T2V/I2V, start-and-end frames, native audio, and reference workflows | Needs review; community-reported endpoint status | Hosted terms apply. Do not generalize behavior from a 2.6 or O1 endpoint to VIDEO 3.0. | [Official VIDEO 3.0 guide](https://app.klingai.com/cn/quickstart/klingai-video-3-model-user-guide) |
| Seedance 2.0 / 2.0 Fast | Hosted / API | `dreamina-seedance-2-0-260128`, `dreamina-seedance-2-0-fast-260128`; text/image/audio/video references, joint audio-video generation, editing, and extension | Needs review; community-reported endpoint status | Hosted terms apply. Official documentation identifies the model IDs and capabilities; it does not certify low-filter behavior. | [Official model page](https://seed.bytedance.com/en/seedance2_0) · [ModelArk API docs](https://docs.byteplus.com/api/docs/ModelArk/2298881) |
| Seedance 1.5 Pro | Hosted / API | `seedance-1-5-pro-251215`; native audio-video generation, T2V/I2V, lip-sync, and camera control | Needs review; community-reported endpoint status | Hosted terms apply. The official technical page says the model is available through the first-party enterprise API; test the exact deployment. | [Official technical page](https://seed.bytedance.com/en/public_papers/seedance-1-5-pro-a-native-audio-visual-joint-generation-foundation-model) · [ModelArk API docs](https://docs.byteplus.com/api/docs/ModelArk/2298881) |
| Seedance 1.0 Pro / Pro Fast | Hosted / API | `seedance-1-0-pro-250528`, `seedance-1-0-pro-fast-251015`; T2V/I2V and multi-shot generation | Needs review; community-reported endpoint status | Hosted terms apply. Record the exact model ID, region, and date tested. | [Official model page](https://seed.bytedance.com/en/seedance) · [ModelArk API docs](https://docs.byteplus.com/api/docs/ModelArk/2298881) |

Contributors can use the [submission template](.github/ISSUE_TEMPLATE/model-submission.md) to promote an endpoint from **Needs review** after documenting reproducible evidence.

## What this list does not claim

- A text-encoder modification does not guarantee that the video transformer learned every concept or produces coherent motion.
- A local checkpoint is not automatically free of UI, pipeline, post-processing, or optional safety filters.
- “NSFW” or “uncensored” tags do not grant permission to create illegal or non-consensual material.
- A model’s license does not automatically transfer to its base model, training data, outputs, adapter, or hosted deployment.
- A checkpoint’s content label does not establish that its training data was lawfully sourced or that real-person likenesses may be used.

## Safety boundary

Use these resources only for lawful, consensual, and ethical work. Do not create sexual content involving minors, non-consensual intimate imagery, targeted harassment, fraud, impersonation, or other abusive or illegal material. Do not submit real-person sexual examples or personal data to this repository.

## How to add a variant

Open an issue using the [model submission template](.github/ISSUE_TEMPLATE/model-submission.md). Include the exact model ID, base model, file or commit revision, evidence for the uncensored claim, supported video task, resolution and duration, license, and a reproducible local or hosted setup. Prefer model-card and official repository links over screenshots or search-result snippets.
