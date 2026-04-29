# XRCore Training Authoring

[![Unity XR](https://img.shields.io/badge/Unity-XR-111111?style=for-the-badge&logo=unity)](https://unity.com/)
[![XRCore Suite](https://img.shields.io/badge/XRCore-Product%20Suite-0ea5e9?style=for-the-badge)](https://github.com/splibiplay/splibiplay)
[![Architecture](https://img.shields.io/badge/Architecture-Editor--First-6366f1?style=for-the-badge)](https://github.com/splibiplay/xrcore-training-authoring)
[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e?style=for-the-badge)](./LICENSE)

XRCore Training Authoring is the official visual authoring layer for Unity XR teams that need to create guided training content at production scale.

Where XRCore SDK provides the event-driven runtime foundation, Training Toolkit provides guided scenario execution, and Assessment provides scoring and certification, Authoring accelerates content creation through an editor-first workflow.

## Why XRCore Training Authoring

Most teams can run training flows but struggle to scale scenario production.

This product solves that by converting manual setup into a repeatable visual pipeline:

- define scenario structure,
- configure steps and conditions,
- generate Toolkit-ready assets,
- generate Assessment-ready wiring,
- generate a playable showcase/demo scene.

## Ecosystem Storytelling

```
Start with XRCore SDK
       ↓
Add Training Toolkit
       ↓
Add Training Assessment
       ↓
Scale with Training Authoring

```

## Relationship with XRCore Ecosystem

This package is intentionally distributed as an extension layer.

- XRCore SDK provides:
  - event bus and modular runtime systems,
  - perception/detection architecture,
  - agent and reasoner foundation.
- XRCore Training Toolkit provides:
  - scenario and step orchestration,
  - validator-driven progression,
  - guided training runtime UX.
- XRCore Training Assessment provides:
  - scoring and pass/fail logic,
  - critical-failure and policy rules,
  - exportable final reports.
- XRCore Training Authoring adds:
  - visual scenario configuration,
  - asset generation pipeline,
  - dependency and preflight gates,
  - release and QA authoring workflow.

## Key Features

- Training Configurator editor workflow
- Step builder with condition presets
- Interaction-signal based workflow authoring
- Demo scene generator with runtime wiring validation
- Preflight gate with safe auto-fixes
- Golden demo lock and release-check automation
- Session report export for demo validation

## XRCore Ecosystem Links

- XRCore ecosystem hub: <https://github.com/splibiplay/splibiplay>
- XRCore SDK: <https://github.com/splibiplay/xrcore-sdk>
- XRCore Training Toolkit: <https://github.com/splibiplay/xrcore-training-toolkit>
- XRCore Training Assessment: <https://github.com/splibiplay/xrcore-assessment>
- SPL organization profile: <https://github.com/splibiplay>

## Documentation

This repository is kept consistent with the XRCore ecosystem style and links.

Core in-project docs live in:

`Assets/TrainingAuthoring/Documentation/`

Recommended release sequence:

1. Validate dependency compatibility
2. Run preflight gate
3. Build package and demo scene
4. Validate golden demo lock
5. Run QA smoke report
6. Run release check report

## License

MIT License
