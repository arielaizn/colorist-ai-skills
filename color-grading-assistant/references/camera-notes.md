# Camera and phone source notes

Use this reference during intake and pipeline selection. It is a decision aid, not a substitute for the camera maker's current manual.

## First classify the source

Identify whether a clip is RAW, Log/flat, a standard display-ready profile, or HDR/phone computational video. Read embedded metadata and inspect a frame, but treat absent or ambiguous tags as unknown. Ask for the model and in-camera profile; verify exact profile support, naming, and limitations in the official model manual. Similar-looking profiles are not interchangeable.

## Phones, especially iPhone

- Ask for the exact phone model, camera app, recording format, profile, HDR/SDR setting, frame rate, and whether the clip was edited or exported before delivery. “Shot on iPhone” is not a color-space specification.
- Apple Log support is model/app dependent. Verify current Apple documentation and clip metadata instead of assuming Apple Log from a washed-out image. A normal/HEVC phone video may already contain sharpening, noise reduction, tone mapping, HDR metadata, and a baked look.
- Keep exposure and white balance stable across takes when possible. For automatic phone capture, look for exposure jumps, changing white balance, clipped skies/skin, mixed indoor lighting, and frame-rate changes. Don't diagnose these as grading errors until the source is checked.
- On HDR material, establish the intended SDR/HDR delivery first. Correctly transform/tone-map once and inspect on a known display path. Avoid stacking phone HDR conversion, an editor transform, and a creative LUT without understanding their order.

## Mirrorless, cinema, action and drone cameras

- Record make/model, exact gamma/gamut or picture profile, bit depth/codec when available, internal/external recording, white balance, and whether the media is original camera footage or a transcode.
- Examples include Sony S-Log/S-Gamut, Canon Log/Cinema Gamut, Panasonic V-Log/V-Gamut, Fujifilm F-Log, DJI D-Log, and manufacturer RAW formats. Names are examples only: verify the actual device, version, recording mode and official transform.
- RAW often exposes debayer, ISO/exposure and white-balance controls; use metadata-aware RAW settings before node-level correction. A transcoded file may no longer support those controls.
- With mixed cameras, map each source into one common working space before matching. Never copy one camera's input transform or LUT to a different camera just because their pictures look similar.

## Log and RAW exposure limits

Log is a recording curve intended for post-production; RAW retains sensor data that can be interpreted later. Neither guarantees a good result. Underexposed, noisy, clipped, incorrectly white-balanced, compressed, or mis-tagged material can still fail. Preserve highlight detail and avoid lifting noisy shadows excessively. If metadata is missing, compare documented candidate transforms on stills and make the uncertainty explicit.

## Baked/standard footage

Treat ordinary display-ready footage as already tone-mapped and sharpened. Make small exposure, white-balance, contrast and saturation changes; inspect skin, gradients, shadows and saturated colors for banding or breakup. Do not force a Log transform onto it. If the requested look exceeds what the source can hold, show a conservative option and explain the compromise.

## Official verification links

- [Apple Support: ProRes/Log recording support on iPhone varies by model](https://support.apple.com/en-ie/109041)
- [Sony S-Log overview](https://helpguide.sony.net/di/pp/v1/en/contents/TP0000909108.html)
- [DaVinci Resolve color management overview](https://www.blackmagicdesign.com/products/davinciresolve/color)
- Use the current device-specific Apple, Canon, Panasonic, Fujifilm, DJI or other vendor support manual for exact profile availability and transforms.
