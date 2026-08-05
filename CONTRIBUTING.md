# Contributing

Thanks for helping keep this list accurate and useful.

## Add a model

Before opening a pull request:

1. Check that the model, adapter, endpoint, or checkpoint is publicly available from a reputable source.
2. Link to the official model card or repository whenever possible.
3. Record the exact checkpoint, file revision, commit, model ID, and inference setup you tested.
4. Record the release date or most recent major update.
5. Identify whether access is local, hosted, API-only, or available in multiple forms.
6. Record the supported task: text-to-video, image-to-video, video-to-video, reference-to-video, speech-to-video, animation, or editing.
7. Include resolution, frame rate, duration, audio behavior, and approximate VRAM or hardware requirements where known.
8. Include the license, commercial-use terms, provider terms, and restrictions from the source.
9. Describe filtering precisely. Separate model behavior from text-encoder behavior, UI settings, provider policy, post-processing, and optional safety checkers.
10. If calling a model “uncensored,” cite the exact evidence and say whether it is a full checkpoint, LoRA, text-encoder modification, pipeline change, or community-reported hosted endpoint.
11. For hosted entries, include the provider, API model ID, snapshot or version, region, UI, date tested, and relevant terms.
12. Do not include private datasets, personal information, real-person sexual examples, or explicit example prompts and outputs.

Use the [model submission issue template](.github/ISSUE_TEMPLATE/model-submission.md) if you are unsure whether an entry is ready.

## Pull request checklist

- [ ] The source link works.
- [ ] The exact version, file, model ID, or commit is identified.
- [ ] Release date or latest major update is identified.
- [ ] Access method is identified: local, hosted, API, or mixed.
- [ ] Video task, resolution, duration, FPS, and audio support are included where known.
- [ ] License and provider terms are included.
- [ ] Hardware and inference details are included where known.
- [ ] “Uncensored” or “low-filter” claims are supported by reproducible notes.
- [ ] Hosted claims identify the exact provider, endpoint, snapshot, region, UI, and test date.
- [ ] The base model and adapter/checkpoint relationship is clear.
- [ ] The entry does not encourage illegal or abusive use.
- [ ] No real-person sexual examples or personal data were added.
- [ ] The README remains alphabetized within its category where practical.

## Corrections and removals

Open an issue when a link, license, model identity, or behavior description is outdated. Include the affected version and a source for the correction. We may remove entries with unclear provenance, incompatible licensing, or repeated inaccurate claims.
