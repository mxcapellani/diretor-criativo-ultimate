# Original Agent vs Ultimate Skill — Comparison Matrix

Version: 1.0.0
Comparison status: PENDING

## Objective

Compare the observable behavior of the original Diretor Criativo agent and Diretor Criativo Ultimate.

Do not assume that a reconstructed specification guarantees identical outputs.

The purpose is functional parity, specialized quality, and regression detection.

## Required setup

Use the same:

- User request.
- Attached files.
- Prior conversation context.
- Creative constraints.
- Output expectations.
- Evaluation rubric.

Record the original agent and Skill runtime details.

Where possible, use identical base models and comparable model settings.

If model or system behavior differs, document the differences as potential confounding factors.

Do not treat literal wording differences as failures when both outputs satisfy the functional requirement.

## Comparison dimensions

Rate each from 0 to 5.

### D1 — Functional coverage

0: Core function missing.
1: Severe loss.
2: Partial function.
3: Adequate.
4: Strong.
5: Complete for the test.

### D2 — Precision

Evaluate clear subjects, accurate interpretation, and technical coherence.

### D3 — Cinematic quality

Evaluate framing, atmosphere, light, visual storytelling, and photographic authenticity.

### D4 — Consistency

Evaluate internal coherence and preservation of established details.

### D5 — Output format

Evaluate code block structure, single-paragraph rule, PARAMS and storyboard gating.

### D6 — Specialty preservation

Evaluate whether the response remains a recognizable cinematography-director deliverable.

### D7 — Autonomy

Evaluate whether the system handles incomplete but solvable requests without unnecessary clarification.

### D8 — Reference fidelity

Evaluate fidelity to supplied imagery, documents, brand details, and prior context.

Mark N/A if no reference is involved.

### D9 — Practical utility

Evaluate readiness for external image/video model use.

### D10 — Advanced functionality

Evaluate relevant refinements such as continuity, platform conversion, and error correction.

For historically unverified Ultimate features, compare whether the enhancement improves quality without breaking core behaviors.

## Exact prompts for paired testing

| ID | Level | Identical request |
|---|---|---|
| C01 | Basic | Make a cinematic prompt about an astronaut walking through a desert at sunrise. |
| C02 | Basic | Create a cinematic scene featuring a red dress in the wind. |
| C03 | Basic | Write a universal cinematic prompt for a mysterious forest at dawn. |
| C04 | Intermediate | Create a Kling 3.0 commercial featuring a black sports car driving through a wet tunnel. |
| C05 | Intermediate | Create a Seedance 2.0 perfume campaign with ivory silk and golden light. |
| C06 | Intermediate | Write a Higgsfield emotional scene of a woman receiving good news on a train. |
| C07 | Intermediate | Create a Nano Banana Pro editorial photograph of a steel mechanical watch on black stone. |
| C08 | Intermediate | Create a cinematic commercial for a sports car. |
| C09 | Complex | Yes, create a 10-shot storyboard based on the previous prompt. |
| C10 | Complex | Analyze the attached image and preserve its lighting and composition in a new hotel setting. |
| C11 | Complex | Adapt the previous prompt for Seedance 2.0 while preserving the product identity. |
| C12 | Complex | Improve this Kling 3.0 prompt: a runner in the rain, camera moving everywhere, epic lighting. |
| C13 | Complex | Write separate Kling 3.0 and Nano Banana Pro prompts for the same model in a white studio. |
| C14 | Complex | Keep the previous scene unchanged except for replacing the camera movement with Orbit/Arc. |
| C15 | Basic | Generate an image of a cinematic futuristic motorcycle. |

## Stateful test dependencies

C09 must follow C08 in the same conversation.

C10 requires the same actual image file in both environments.

C11 requires both environments to receive the same prior product prompt.

C14 requires both environments to receive the same prior scene.

For strict comparability, save prerequisite text and inject identical copies into both environments when native previous responses differ.

Do not compare two different prior prompts as if the full conversational conditions were identical.

## Scoring formula

For every applicable dimension:

    Relative delta = Skill score - Original score

For each test:

    Original average = sum(original scores) / applicable dimensions

    Skill average = sum(skill scores) / applicable dimensions

    Difference = Skill average - Original average

Aggregate:

    Functional preservation rate =
      original capabilities passing in Skill /
      original capabilities actually tested

    Critical format pass rate =
      successful format requirements /
      applicable format requirements

    Advanced extension pass rate =
      successful Ultimate extension requirements /
      tested Ultimate extension requirements

Never count untested requirements as successful.

Report coverage separately from quality scores.

## Measurement guidance

A difference of zero indicates matching rubric performance, not textual identity.

A positive difference indicates a stronger evaluated result.

A negative difference indicates a potential regression requiring review.

Platform-dependent differences may result from the underlying model, not only the Skill.

Repeat each prompt at least three times when the model is nondeterministic.

If reproducible settings or seeds are available, record them.

## Results table

| Test | Original avg. | Skill avg. | Delta | Status |
|---|---:|---:|---:|---|
| C01 | — | — | — | Pending |
| C02 | — | — | — | Pending |
| C03 | — | — | — | Pending |
| C04 | — | — | — | Pending |
| C05 | — | — | — | Pending |
| C06 | — | — | — | Pending |
| C07 | — | — | — | Pending |
| C08 | — | — | — | Pending |
| C09 | — | — | — | Pending |
| C10 | — | — | — | Pending |
| C11 | — | — | — | Pending |
| C12 | — | — | — | Pending |
| C13 | — | — | — | Pending |
| C14 | — | — | — | Pending |
| C15 | — | — | — | Pending |

## Regression classification

### Critical

- Loss of cinematic prompt generation.
- Loss of text-only operation.
- Loss of required English prompt output.
- Loss of core format.
- Automatic unwanted storyboard.
- Invention of unseen reference details.

### Major

- Repeated camera contradictions.
- Weak platform adaptation.
- Failure to preserve subject identity.
- Major brand inconsistency.
- Ignored explicit constraints.

### Minor

- Weaker creative specificity.
- Minor redundancy.
- Less effective lens recommendation.
- Reduced atmospheric detail.
- Less elegant narrative pacing.

## Feature verification inventory

| Capability | Specification status | Runtime evidence |
|---|---|---|
| Cinematic English paragraph | Preserved | Pending |
| One main code block | Preserved | Pending |
| PARAMS output | Preserved | Pending |
| Storyboard on confirmation | Preserved | Pending |
| Authorized shot vocabulary | Preserved | Pending |
| Kling profile | Preserved | Pending |
| Seedance profile | Preserved | Pending |
| Higgsfield profile | Preserved | Pending |
| Nano Banana Pro profile | Preserved | Pending |
| Visual-reference analysis | Conditional | Requires image fixture |
| Brand-context interpretation | Preserved | Pending |
| Context retention | Preserved | Pending |
| Prompt refinement | Ultimate extension | Pending |
| Cross-platform conversion | Ultimate extension | Pending |
| Continuity review | Ultimate extension | Pending |
| Contradiction repair | Ultimate extension | Pending |
| Multi-scene output | Ultimate extension | Pending |

## Equivalence decision

Possible outcomes:

- Not evaluated.
- Insufficient evidence.
- Partial functional preservation.
- Strong functional preservation.
- Functional parity demonstrated for the tested scope.
- Functional parity with documented improvements.

Do not declare full equivalence from a subset of tests.

## Release evaluation template

Original agent:
Original model/runtime:
Skill host:
Skill model/runtime:
Skill version:
Test date:
Tests executed:
Original average:
Skill average:
Functional preservation rate:
Critical regressions:
Major regressions:
Ultimate extensions validated:
Unverified capabilities:
Overall conclusion:
Reviewer:

## Current verdict

INSUFFICIENT EVIDENCE.

The specification preserves all identifiable core capabilities.

No original-versus-Skill paired runtime evaluation has yet been performed.

Full equivalence is not claimed.
