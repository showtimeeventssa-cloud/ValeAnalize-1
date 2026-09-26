# ValeAnalize V27 — Correct Home Logo

GitHub-ready build based on V26. GP-50/audio functionality is retained.

Branding repair only: the supplied ValeAnalize guitar-pick + guitar neck/headstock + blue waveform logo is used for the iOS Home Screen icon, PWA icons, and embedded header/main artwork. The header and main artwork are embedded directly in `index.html`.

The ShowCue package was used as the structural reference for self-contained branding and Apple Home Screen icon handling.

Important: iOS may retain an old Home Screen icon. Delete the old ValeAnalize shortcut and add the current GitHub Pages site to the Home Screen again after deployment.


## V28 Accuracy Engine
- Preserves V27 branding/assets.
- Replaces simple whole-file averaging with frame-level guitar-likelihood selection, robust trimmed statistics and optional section selection.
- High Accuracy / Guitar Focus / Auto Section Detection switches now actually control analysis state.
- Distortion/gain estimate uses harmonic structure + dynamics rather than crest factor alone.
- Analysis reports an evidence-quality percentage and selected-frame count; this is explicitly not a claim of recovering an unknown original studio preset.
- Acoustic target uses AC Pre1/AC Pre2 and AC BA routing; electric target uses documented GP-50 amp/cab families.
- GP-50 binary export retains the validated source/template model IDs rather than guessing undocumented model IDs.


## V30 artwork-only rebuild
V30 keeps the V28 application logic and GP-50 accuracy engine unchanged. Only the embedded artwork/logo, PWA icon family, manifest references and service-worker cache were rebuilt.


## V31 Precision Guitar Engine
V31 keeps the V30 artwork and V28 GP-50 engine, but upgrades reference analysis for guitar: phase-safe stereo handling, dedicated stem priority, YIN-style pitch/confidence tracking, harmonic-frame selection, spectral flux, slope, weighted spectral envelope, and spectral-envelope-aware calibration. The supplied 552-byte Soos Bloed GP-50 preset is included as a reference fixture.
