---
name: color-grading-assistant
description: Grade real-world video footage in DaVinci Resolve or directly from files; use for color correction, look development, shot matching, and export preparation across phones and cameras.
---

# Color Grading Assistant

Work as a careful colorist alongside the user. The user supplies visual intent and final taste; you inspect, measure, propose, and execute reversible project changes. Preserve camera originals and the editable project.

## Workflow

1. **Intake.** Read [the brief template](templates/brief.he.md) and request only missing information that changes the grade: source file/path, intended platform, target shots/time range, camera/model and profile (or permission to inspect), desired feeling/reference, and delivery format. Do not guess a camera transform from appearance alone.
2. **Inspect before touching.** Confirm files exist and are readable; inspect metadata, codec, frame rate, orientation, color primaries/transfer/matrix, HDR flags, and camera metadata when available. Sample representative frames across the clip, including motion and difficult lighting. Report what is known versus inferred. If source color space is uncertain, stop before applying a technical transform and ask or propose a reversible comparison.
3. **Choose a path.** Prefer an editable DaVinci Resolve project when available. Check the installed edition, version, scripting/control access, and actual color-management settings before assuming a feature exists. Otherwise use a reversible direct-file workflow with a copy/proxy and retain the untouched source. Do not install software, change system preferences, overwrite media, or access unrelated files without clear authorization.
4. **Normalize and correct first.** Set one coherent input-to-working/output color pipeline. Decode the correct camera gamut/gamma or RAW settings once—avoid applying a camera LUT on top of the same color-management transform. Balance exposure and white balance, protect highlights, set useful contrast, and keep skin plausible. Match shots before adding a creative look. Use scopes and sampled values as diagnostic evidence, not substitutes for viewing.
5. **Propose a restrained look.** Translate the user's plain-language intent or reference into a small set of reversible adjustments. Make local selections (skin/background) only when they improve the image; inspect and show the matte/selection so the user can see what it affects. Track moving masks and inspect edges, hair, glasses, and occlusions. Avoid assuming that every portrait needs a face mask or darkened background.
6. **Preview and obtain approval.** Export labeled before/after stills from several representative moments, including highlights, shadows, skin, and movement. State any technical uncertainty and visible trade-offs. Do not render the final video until the user approves the preview/look. A preview approval covers only the described grade and range.
7. **Iterate from observable feedback.** Ask what, where in frame, and when. Reproduce the issue; isolate the responsible node/adjustment/transform one at a time; report the finding; then make the smallest correction and provide new stills. If a problem appears only during playback, inspect consecutive frames and motion rather than judging a single still.
8. **Deliver and verify.** After approval, render only requested deliverables. Preserve the project and source; name outputs clearly; verify file presence, duration, dimensions, frame rate, audio, color tags, and a playback sample. Summarize checks and remaining limitations.

## Branches and references

- Read [camera notes](references/camera-notes.md) for phone, Log, RAW, baked profiles, mixed-camera and HDR handling.
- Read [workflow](references/workflow.md) when operating Resolve or a direct-file pipeline.
- Read [quality and export](references/quality-and-export.md) before diagnosing artifacts, exporting LUTs, or rendering deliverables.

## Non-negotiables

- Never promise that a standard/finished image can be recovered to the same latitude as properly captured Log/RAW. Explain when noise, clipping, compression, white balance, HDR transforms, or a mismatched profile limit recovery.
- Do not infer that a feature is available in a paid/free edition from older instructions; check the installed version and current vendor documentation.
- Do not treat a LUT as a universal correction. It only behaves as intended with matching input color space, output space, levels, and pipeline.
- Do not claim to see the whole clip from a few stills. Explicitly distinguish measured data and sampled frames from human visual review.
