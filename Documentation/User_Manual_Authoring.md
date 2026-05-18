# XRCore Training Authoring - User Manual

## Audience

This manual is for training designers, technical artists, and developers using `XRCore Training Authoring` to build XR training scenarios in Unity.

## Demo Video

See the full Authoring walkthrough:

- [XRCore Training Authoring Demo](https://youtu.be/Y9-OmcG0lpQ)

## Goal

Create a complete training flow without manual runtime wiring:

- scenario definition
- step sequence
- completion conditions
- validators and assessment profile
- generated assets
- playable demo scene

## Prerequisites

Make sure your Unity project includes:

- XRCore SDK
- XRCore Training Toolkit
- XRCore Training Assessment
- XRCore Training Authoring

Recommended:

- Unity 6.x (LTS preferred)

## Open the Tools

Use:

- `Tools -> XRCore -> General -> Authoring -> Setup Wizard`
- `Tools -> XRCore -> General -> Authoring -> Training Configurator`

If you are new, start with `Setup Wizard`.

## Authoring Workflow (Step by Step)

1. Create the scenario shell.
2. Define and order steps.
3. Define completion conditions for each step.
4. Configure validators.
5. Configure assessment profile.
6. Run preflight auto-fix.
7. Build training assets.
8. Generate demo scene.
9. Validate in Play Mode.

## 1) Create Scenario Shell

In `Training Configurator`, set:

- `Scenario Name`
- `Scenario ID` (stable ID, keep it constant across revisions)
- scenario description

## 2) Create and Order Steps

For each step:

- set a unique `stepId`
- set `title` and `instruction`
- choose `stepType`
- set mandatory flag and `weight`

Supported step types:

- Look
- Grab
- Place
- Validation
- Checklist
- Decision
- Safety
- Custom

## 3) Define Completion Conditions

Typical condition types:

- `LookAtTarget`
- `ProximityToTarget`
- `ActionKeyPress`
- `HoldObject`
- `WaitSeconds`
- `InteractionSignal`

Important:

- If a step has no conditions, safe defaults can be generated.
- Non-custom interaction presets are normalized to canonical signals.
- `expectedSignal` is synchronized from conditions.

## 4) Configure Validators

Attach validator bindings per step to define what "valid completion" means.

Best practice:

- start simple with one clear validator per step
- add strict validation only when operationally required

## 5) Configure Assessment Profile

Define:

- pass score
- critical failure behavior
- scoring weight influence

Keep weights aligned with real safety and operational impact.

## 6) Run Preflight

Run:

- `Run Preflight Gate + Auto-Fix (Safe)`

Pass criteria:

- no blocking `ERROR` in the report

## 7) Build Training Assets

Click:

- `Build Training Package`

This creates generated scenario artifacts ready for Toolkit/Assessment runtime integration.

## 8) Generate Playable Demo Scene

Click:

- `Create Playable Demo Scene`

The scene is generated from the current scenario configuration and includes mapped interactables according to step conditions.

## 9) Validate in Play Mode

In Play Mode, verify:

- step order and completion logic
- interactable behavior (button/wheel/lever/joystick)
- instruction and progress UX clarity

## One-Click Full Check

Use:

- `Tools -> XRCore -> General -> Authoring -> Self Diagnose (Preflight + Generate + Validate)`

## Troubleshooting

### Demo scene does not reflect latest changes

- regenerate after updating steps/conditions
- confirm scenario name/ID is the intended one

### Step does not complete

- verify condition match mode (`All` vs `Any`)
- verify expected signal vs interaction signal
- verify target role mapping

### Wrong interactable mapped

- use explicit `InteractionSignal` preset in conditions
- regenerate demo scene

### Interaction feels inconsistent

- validate generated wiring using Self Diagnose
- ensure the scenario conditions are deterministic

## Release Checklist (Short)

Before publishing:

1. Dependency compatibility check passes.
2. Preflight passes.
3. Build package + demo scene generation pass.
4. QA smoke/golden checks pass.
5. Release report is PASS.

## Practical Tips

- Prefer action verbs in step titles (`Inspect`, `Grab`, `Validate`).
- Keep instructions short and explicit.
- Split complex operations into smaller steps.
- Validate every step in Play Mode before adding complexity.
