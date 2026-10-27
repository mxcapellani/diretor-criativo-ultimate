# Acceptance Test Suite

Version: 1.0.0
Execution status: NOT EXECUTED

## Purpose

Verify that Diretor Criativo Ultimate satisfies its operational specification.

These are behavioral tests, not claims about visual generation quality.

## Test procedure

For each test:

1. Start a fresh conversation unless context retention is under test.
2. Activate the skill.
3. Submit the exact test request.
4. Save the unmodified response.
5. Evaluate required behaviors.
6. Record failures and deviations.
7. Repeat where consistency matters.

## Shared production assertions

A standard production response must:

- Include one English cinematic paragraph inside a code block.
- Include a PARAMS line outside the code block.
- Provide meaningful lighting direction.
- Describe atmospheric behavior or controlled atmosphere.
- Describe relevant subject-environment interaction.
- Use authorized cinematic terminology.
- Avoid engine-rendering buzzwords.
- Avoid contradictory camera instructions.
- Avoid direct visual generation.
- Ask the storyboard question unless already requested.

## Acceptance cases

### AT-01 — Minimal brief

Level: Basic

Input:

"Make a cinematic scene of a lone astronaut walking across a desert."

Expected:

- Complete scene.
- Coherent astronaut and desert details.
- Camera distance and angle.
- Lighting and atmospheric dust.
- Physical walking interaction.
- Standard output format.

Status: NOT EXECUTED

### AT-02 — Brand commercial

Level: Intermediate

Input:

"Create a premium watch commercial for an elegant minimalist brand, with a dark blue and silver palette."

Expected:

- Faithful use of stated palette.
- Premium product emphasis.
- Authentic material reflections.
- No invented official logo.
- Recognizable watch details.

Status: NOT EXECUTED

### AT-03 — Kling 3.0 motion

Level: Intermediate

Input:

"Write a Kling 3.0 video prompt for a black car accelerating through a wet tunnel at night."

Expected:

- Defined primary movement.
- Controlled camera trajectory.
- Stable subject identity.
- Coherent wet-surface reflections.
- Sensible video duration.

Status: NOT EXECUTED

### AT-04 — Seedance 2.0 atmosphere

Level: Intermediate

Input:

"Create a Seedance 2.0 perfume advertisement with ivory silk, golden light, and gentle movement."

Expected:

- Smooth controlled action.
- Meaningful fabric motion.
- Atmospheric depth.
- Product remains visually dominant.
- Physically plausible lighting.

Status: NOT EXECUTED

### AT-05 — Higgsfield emotion

Level: Intermediate

Input:

"Create a Higgsfield scene of a woman receiving unexpected good news during a train journey."

Expected:

- Legible emotional progression.
- Subtle face and body behavior.
- Intimate framing.
- Credible train-window lighting.
- No unnecessary dialogue.

Status: NOT EXECUTED

### AT-06 — Nano Banana Pro still

Level: Intermediate

Input:

"Write a Nano Banana Pro prompt for a brushed-steel wristwatch photographed on black stone."

Expected:

- Static visual construction.
- Material-specific detail.
- Reflection and shadow control.
- Still-image duration marked N/A.
- Editorial photographic quality.

Status: NOT EXECUTED

### AT-07 — Incomplete instruction

Level: Basic

Input:

"Something cinematic with a red dress."

Expected:

- No mandatory clarification.
- Coherent fashion direction.
- Respectful subject description.
- Usable finished prompt.

Status: NOT EXECUTED

### AT-08 — Storyboard gating

Level: Intermediate

Input:

"Create a cinematic commercial for a sports car."

Expected:

- Prompt and PARAMS.
- Storyboard question.
- No unrequested storyboard.

Status: NOT EXECUTED

### AT-09 — Storyboard confirmation

Level: Intermediate

Prerequisite:

Complete AT-08.

Follow-up input:

"Yes, create the storyboard."

Expected:

- ACT structure.
- 8–12 shots by default.
- Sequential shot numbering.
- Authorized shot terminology.
- Original scene continuity.
- No repeated storyboard question.

Status: NOT EXECUTED

### AT-10 — Prompt improvement

Level: Intermediate

Input:

"Improve this Kling 3.0 prompt: A runner in the rain, camera moving everywhere, epic light, dramatic action."

Expected:

- Subject and intended mood preserved.
- Ambiguous motion removed.
- Physically coherent camera plan.
- Specific light sources or behavior.
- Standard production response.

Status: NOT EXECUTED

### AT-11 — Reference fidelity

Level: Complex

Input:

"Use the attached reference image for framing and lighting, but move the subject into an elegant hotel lobby."

Fixture:

An actual image supplied during runtime.

Expected:

- Only observable image details reported.
- Key framing and light characteristics preserved.
- Environment changed as requested.
- No false claim of visual access.
- Normal cinematic output.

Status: REQUIRES IMAGE FIXTURE AND EXECUTION

### AT-12 — Contextual continuity

Level: Complex

Turn 1:

"Create a cinematic commercial featuring a silver sports car on a coastal road at sunrise."

Turn 2:

"Keep everything, but change the camera movement to Orbit/Arc."

Expected:

- Silver car preserved.
- Coastal road preserved.
- Sunrise preserved.
- Camera movement changed.
- No unnecessary complete concept reset.

Status: NOT EXECUTED

### AT-13 — Cross-platform conversion

Level: Complex

Input:

"Turn this Nano Banana Pro still prompt into an eight-second Seedance 2.0 video without changing the watch or its materials."

Prerequisite:

A previous still prompt with specified product features.

Expected:

- Product identity remains stable.
- New motion is physically meaningful.
- Still-only instructions adapted.
- Product materials unchanged.
- Video duration correct.

Status: NOT EXECUTED

### AT-14 — Unsupported platform

Level: Basic

Input:

"Create a cinematic prompt for an unfamiliar image generator called ExampleVision."

Expected:

- Universal-mode fallback.
- No invented proprietary settings.
- Usable prompt.
- Normal parameter line.

Status: NOT EXECUTED

### AT-15 — No image generation

Level: Basic

Input:

"Generate the image of a futuristic motorcycle right now."

Expected:

- Cinematic text prompt only.
- No generation tool invocation.
- No claim an image has been created.
- PARAMS line and storyboard behavior.

Status: NOT EXECUTED

### AT-16 — Complex multi-shot narrative

Level: Complex

Input:

"Create a 10-shot storyboard for a premium electric-car commercial, beginning before sunrise and ending with the vehicle on a mountain overlook."

Expected:

- Complete cinematic prompt.
- PARAMS line.
- Ten numbered shots.
- Coherent progression.
- Consistent car identity.
- Logical time progression.
- No additional storyboard confirmation.

Status: NOT EXECUTED

### AT-17 — Contradiction repair

Level: Complex

Input:

"Improve this scene: the camera stays Static while simultaneously circling the subject at high speed, and all shadows point toward different suns."

Expected:

- Incompatibilities resolved.
- Original cinematic intention retained.
- Realistic lighting logic.
- No contradictory movement instructions.

Status: NOT EXECUTED

### AT-18 — Multiple platforms

Level: Complex

Input:

"Write separate prompts for Kling 3.0 and Nano Banana Pro showing the same fashion model in the same white studio."

Expected:

- Two separate prompts.
- Each prompt contains one paragraph.
- Video behavior adapted for Kling.
- Still-image behavior adapted for Nano Banana Pro.
- Stable wardrobe, identity and environment.
- Distinct PARAMS lines.

Status: NOT EXECUTED

## Pass/fail criteria

Each applicable assertion is scored:

- PASS: requirement satisfied.
- PARTIAL: substantially satisfied with a material defect.
- FAIL: requirement not satisfied.
- N/A: requirement does not apply.
- BLOCKED: cannot execute or evaluate.

Critical failures:

- Generated a visual asset instead of text.
- Omitted the main cinematic prompt during production.
- Violated storyboard gating.
- Lost explicit subject identity.
- Introduced physically contradictory camera direction.
- Claimed to have inspected inaccessible reference material.

## Acceptance threshold

For release readiness:

- All critical assertions must pass.
- At least 90% of applicable assertions must pass.
- No unreviewed failures involving brand/reference fidelity.
- All supported platform profiles must pass their dedicated tests.
- All output-contract tests must pass.

This threshold is a release criterion, not an achieved result.

## Regression procedure

After every skill update:

1. Rerun all previously passed tests.
2. Compare against the prior release.
3. Identify new failures.
4. Resolve critical regressions.
5. Update CHANGELOG.md.
6. Record the tested agent runtime and model.

## Test record template

Test ID:
Date:
Agent runtime:
Model:
Skill version:
Actual output:
Applicable assertions:
Passed:
Partial:
Failed:
Blocked:
Reviewer:
Notes:

## Current conclusion

No acceptance tests have been executed as part of the initial specification package.

Functional readiness remains unverified until the tests run.
