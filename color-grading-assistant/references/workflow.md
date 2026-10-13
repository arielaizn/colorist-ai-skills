# Operating workflow

## DaVinci Resolve path

1. Confirm Resolve is open, project/media paths are correct, and the installed edition/version supports the intended operation. Do not assume remote scripting, scripting location permissions, or Studio-only tools are enabled. Ask before installing dependencies or changing preferences.
2. Duplicate or version the project before edits. Keep the source media untouched. Confirm timeline frame rate, resolution, color science, input transforms, output target, and monitoring assumptions.
3. Use a clear node plan where each stage has one purpose: source decode/color management; balance; shot matching; optional local isolation/tracking; creative look; output trim. Avoid duplicate transforms. Use clip/group/timeline nodes only when the scope is explicit.
4. Work on representative clips first. Compare scopes and frames, then propagate settings only to genuinely matching shots. Check cuts and lighting changes after propagation.
5. Render reference stills to the requested location and show them for approval before final rendering. Keep approved settings reversible and identify what the user approved.
6. After approval, render to a new output path; do not overwrite camera originals or previous finals. Reopen/inspect the result and the saved project.

## Direct-file path (without Resolve Studio)

Use a file-based processing toolchain only after confirming it exists and supports the input codec, metadata, color transform, frame rate and output format. Keep intermediate stages reversible, retain the original, and document the transform chain. Do not present a LUT-only workflow as identical to an editable Resolve grade. A LUT can encode only a bounded color transform and cannot replace masks, tracking, temporal fixes or all source-camera decoding steps.

For a LUT deliverable, specify the input and output color spaces and the point in the pipeline where it should be applied. Generate a test clip/still through the target application and compare against the approved reference before claiming compatibility. Different applications may interpret LUT data and levels differently.

## User communication

Use nontechnical descriptions first (“the window is clipping”, “skin is too magenta”). Introduce technical terms only to explain a real choice. Ask one concise question at a time when the answer blocks safe pipeline selection. Be explicit about any action that requires a click or cannot be automated.
