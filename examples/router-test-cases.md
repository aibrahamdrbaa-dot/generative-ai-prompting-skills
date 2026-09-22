# Router Test Cases

These cases are regression tests for architecture, not model benchmarks.

## Case 1 — Property walkthrough video

Request: Create a realistic 20-second property walkthrough using a room image as the opening frame.

Expected stack:
- Visual Brief
- Model Router
- Video Storyboard
- Visual Bible if rooms/objects repeat
- Cinematic or Photorealism if triggered
- Gemini Omni 1.1 Flash adapter
- Quality Gate
- Iteration Controller if needed

Reason code: VIDEO_NATIVE

## Case 2 — Real-estate interior from multiple references

Request: Combine this floor plan, this empty-room photo, and this furniture reference into a polished listing image.

Expected stack:
- Visual Brief
- Reference Manager
- Real Estate specialty
- Architectural Visualization style
- Nano Banana 2 or Pro depending on constraint density
- Prompt Compiler
- QA

Do not let the style reference override room geometry.

## Case 3 — Exact background edit

Request: Replace only the background and keep the person, pose, face and clothing unchanged.

Expected stack:
- Visual Editing
- Reference Manager if reference exists
- Model adapter
- Quality Gate
- Iteration Controller

The prompt must explicitly preserve the invariants.

## Case 4 — Text-heavy social graphic

Request: Create an Arabic announcement with the exact headline and a strict 4:5 layout.

Expected stack:
- Typography & Layout
- Prompt Compiler
- selected image model
- Quality Gate

Exact text must be copied verbatim.

## Case 5 — Same character across five shots

Expected stack:
- Visual Bible
- Video Storyboard
- Reference Manager
- Gemini Omni 1.1 Flash for video
- Quality Gate after the sequence, not only per-shot

Regression target: minimize identity and wardrobe drift.
