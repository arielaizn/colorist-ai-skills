# Quality checks and delivery

## Preview set

Choose multiple moments: a representative face, brightest highlight, darkest useful shadow, saturated color, and a moving section with any mask/tracking. Include shots from different lighting setups. Label each still with timecode, version, and whether it is source, normalized correction, or creative look.

## Diagnose problems

- **Unnatural skin:** inspect white balance, mixed light, saturation and any skin selection. Verify what the mask captures; don't solve every skin issue by globally warming the image.
- **Clipped/flat highlights:** check source and transform before lowering gain. Recover only if source detail exists; a pure white region contains no recoverable texture.
- **Color blotches/banding:** compare against the original, inspect bit depth/compression, and reduce aggressive saturation/contrast/shadow lifts. Don't hide damaged pixels with an unapproved heavy blur.
- **Flicker/pumping:** inspect consecutive frames for auto-exposure, auto-white-balance, changing light, noise reduction or tracking instability. Separate source flicker from grade-induced temporal changes.
- **Mask halos/track slips:** inspect edges and occlusions during playback; refine/soften or remove the local correction if it looks worse than the problem.
- **Mismatched shots:** check source transforms, white balance, exposure and lighting first; match neutral and skin relationships before imposing a shared look.

## Final checks

Verify at minimum:

- File exists, opens, and plays from beginning, middle and end.
- Duration, frame size, orientation and frame rate match the requested delivery.
- Expected audio is present and not unintentionally muted/clipped.
- Color primaries, transfer and matrix tags match the declared output intent; confirm HDR metadata when relevant.
- No black frames, dropped/frozen sections, unexpected crop, mask failures, obvious cut mismatches or render artifacts.
- Project opens and retains media links, transforms and nodes; camera originals remain unmodified.

Report exactly what was checked and what still needs human review on the intended phone/social platform. An export check cannot certify that every display will show identical color.
