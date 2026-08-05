---
name: Model submission
about: Suggest an AI video model, checkpoint, adapter, or endpoint for the catalog
title: "Add model: "
labels: model-submission
assignees: ""
---

## Model

- Name and exact version:
- Official model card or repository:
- Download or API link:
- Base architecture / required base model:
- Component type: full checkpoint, LoRA, text encoder, quantization, pipeline change, or hosted endpoint
- Video task: T2V, I2V, V2V, R2V, S2V, animation, or editing

## Video capabilities

- Resolution and aspect ratios:
- Frame rate and maximum duration:
- Audio support:
- Recommended hardware or VRAM:
- Inference tools/workflows tested:
- File revision, commit, or model snapshot:
- Date tested:

## Licensing

- License:
- Commercial use allowed? Please link to the relevant terms:
- Provider or hosted-service terms, if applicable:

## Uncensored / low-filter evidence

- Is this a full checkpoint, LoRA, text encoder, pipeline change, or hosted endpoint?
- If hosted/API-based, what exact provider, endpoint, model ID, snapshot, region, UI, and date were tested?
- What exact upstream text, tags, tests, or release notes support the claim?
- What base model, VAE, text encoder, or adapter is required?

## Filtering behavior

Describe what you tested and distinguish between model behavior, text-encoder refusals, pipeline safety checkers, provider moderation, post-processing, and UI settings. Do not include abusive or illegal example prompts or outputs.

## Checklist

- [ ] The source is public and reputable.
- [ ] The exact version, file, model ID, or commit is identified.
- [ ] The video task and output limits are documented.
- [ ] License and provider terms are linked.
- [ ] The uncensored/low-filter claim is sourced and clearly labeled as creator-reported or independently tested.
- [ ] The base model and component relationship is clear.
- [ ] The information above is reproducible.
- [ ] No real-person sexual examples or personal data are included.
