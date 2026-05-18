# XRCore Training Authoring

[![Unity](https://img.shields.io/badge/Unity-2022%2B%20%7C%20Unity%206-black)](https://unity.com/)
[![Module](https://img.shields.io/badge/Module-Authoring%20Layer-2563eb)](#)
[![Mode](https://img.shields.io/badge/Mode-Editor--First-7a3cff)](#)
[![Output](https://img.shields.io/badge/Output-Scenarios%20%2B%20Playable%20Demo-0ea5e9)](#)
[![License](https://img.shields.io/badge/License-MIT-22c55e)](LICENSE)

Official XRCore module for visual XR training scenario creation in Unity.

## Foundation (Unity Asset Store)

Install XRCore foundation first:

- [XRCore – Event-Driven AI Framework for Unity XR](https://assetstore.unity.com/packages/tools/ai-ml-integration/xrcore-event-driven-ai-framework-for-unity-xr-366852)

## What This Module Does

`xrcore-training-authoring` converts manual training setup into a repeatable editor workflow:

- visual scenario and step authoring
- completion-condition authoring (including interaction signals)
- validator assignment and assessment profile setup
- generated runtime-ready assets
- generated playable demo scene
- preflight, smoke, and release-oriented checks

## Current Functional State (Updated)

The module currently includes:

- dynamic demo generation from the **current** authoring configuration
- completion contract normalization (`conditions` as source of truth)
- expected signal synchronization from conditions
- deterministic interactable mapping (Wheel / Lever / Joystick / Button)
- post-generation scene wiring validation
- one-click self-diagnose flow (preflight + generate + validate)
- improved demo interaction behavior (grab/place and engaged interaction flow)
- EditMode test coverage for completion contract + interactable mapping

## Quick Start

1. Open `Tools -> XRCore -> General -> Authoring -> Setup Wizard`.
2. Open `Training Configurator`.
3. Define scenario metadata (`Scenario Name`, `Scenario ID`, description).
4. Create and order steps.
5. Define completion conditions and validators.
6. Run `Run Preflight Gate + Auto-Fix (Safe)`.
7. Click `Build Training Package`.
8. Click `Create Playable Demo Scene`.
9. Enter Play Mode and validate the full flow.

## Authoring Demo Video

Watch the full authoring demo on YouTube:

- [XRCore Training Authoring Demo](https://youtu.be/Y9-OmcG0lpQ)

[![Watch the demo](https://img.youtube.com/vi/Y9-OmcG0lpQ/hqdefault.jpg)](https://youtu.be/Y9-OmcG0lpQ)

## One-Click Health Check

- `Tools -> XRCore -> General -> Authoring -> Self Diagnose (Preflight + Generate + Validate)`

## User Documentation

- Full manual: `Documentation/User_Manual_Authoring.md`

This manual is written for content teams and developers and explains:

- end-to-end workflow
- completion conditions and interaction presets
- validator and assessment setup
- troubleshooting and release checklist

## Ecosystem Position

```text
SDK + Toolkit + Assessment
           ↓
Training Authoring
           ↓
Voice / VisionPlus / LLBridge / Analytics
```

## Related XRCore Modules

[![Hub — splibiplay](https://img.shields.io/badge/Hub-splibiplay-24292f?style=flat-square)](https://github.com/splibiplay/splibiplay)
[![Unity Asset Store — XRCore](https://img.shields.io/badge/Unity%20Store-XRCore-f59e0b?style=flat-square)](https://assetstore.unity.com/packages/tools/ai-ml-integration/xrcore-event-driven-ai-framework-for-unity-xr-366852)

[![xrcore-sdk](https://img.shields.io/badge/GitHub-xrcore--sdk-2563eb?style=flat-square)](https://github.com/splibiplay/xrcore-sdk)
[![xrcore-context](https://img.shields.io/badge/GitHub-xrcore--context-0e7490?style=flat-square)](https://github.com/splibiplay/xrcore-context)
[![xrcore-training-toolkit](https://img.shields.io/badge/GitHub-training--toolkit-7c3aed?style=flat-square)](https://github.com/splibiplay/xrcore-training-toolkit)
[![xrcore-assessment](https://img.shields.io/badge/GitHub-assessment-db2777?style=flat-square)](https://github.com/splibiplay/xrcore-assessment)
[![xrcore-training-authoring](https://img.shields.io/badge/GitHub-authoring-c2410c?style=flat-square)](https://github.com/splibiplay/xrcore-training-authoring)
[![xrcore-voice](https://img.shields.io/badge/GitHub-voice-059669?style=flat-square)](https://github.com/splibiplay/xrcore-voice)
[![xrcore-visionplus](https://img.shields.io/badge/GitHub-vision--plus-0f766e?style=flat-square)](https://github.com/splibiplay/xrcore-visionplus)
[![xrcore-llbridge](https://img.shields.io/badge/GitHub-llbridge-4f46e5?style=flat-square)](https://github.com/splibiplay/xrcore-llbridge)
[![xrcore-analytics](https://img.shields.io/badge/GitHub-analytics-d97706?style=flat-square)](https://github.com/splibiplay/xrcore-analytics)
[![xrcore-ai](https://img.shields.io/badge/GitHub-xrcore--ai-9333ea?style=flat-square)](https://github.com/splibiplay/xrcore-ai)
[![xrcore-ai-mcp](https://img.shields.io/badge/GitHub-xrcore--ai--mcp-7c3aed?style=flat-square)](https://github.com/splibiplay/xrcore-ai-mcp)

## License

MIT License.
