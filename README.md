# Diretor Criativo™ Ultimate

**Portable Cinematic Prompt Director — Agent Skills Edition**

Version: 1.0.0

A professional Agent Skill that converts creative briefs, visual references, brand contexts, and cinematic concepts into polished English prompts for external image and video generation systems.

## Overview

Diretor Criativo Ultimate preserves the specialized identity of the original Diretor Criativo agent.

It is a cinematic creative director, not an image-generation engine.

Its primary responsibility is to produce filmically coherent directions for external tools.

The skill emphasizes:

- Cinematic framing.
- Credible photography and lighting.
- Physically coherent motion.
- Environmental atmosphere.
- Subject-environment interaction.
- Commercial art direction.
- Brand consistency.
- Platform-aware prompt construction.
- Storyboards on request.

## Supported platforms

| Platform | Primary specialization |
|---|---|
| Kling 3.0 | Motion, camera trajectories, subject anchoring |
| Seedance 2.0 | Smooth motion, atmosphere, environmental interaction |
| Higgsfield | Micro-expression, body language, emotional narrative |
| Nano Banana Pro | Photorealistic stills, materials, lighting and texture |
| Universal | Tool-independent cinematic direction |

These integrations are prompt-writing profiles, not API connections.

No platform-specific API compatibility is guaranteed.

## Preserved functionality

The skill preserves these identifiable behaviors:

1. Creative brief interpretation.
2. Cinematic English prompt generation.
3. One-paragraph production prompts.
4. Camera shot and movement control.
5. Atmospheric and lighting direction.
6. Brand-context adaptation.
7. Platform-specific creative emphasis.
8. Visual-reference interpretation where supported.
9. Automatic creative inference from incomplete briefs.
10. Aspect ratio, duration and lens recommendations.
11. Storyboard generation after confirmation.
12. Controlled cinematic shot vocabulary.
13. Text-only production.
14. No direct visual generation.

The original agent's complete historical behavior has not been empirically verified.

## Ultimate enhancements

Version 1.0.0 adds:

- Prompt refinement.
- Cross-platform adaptation.
- Shot-continuity review.
- Lighting and physics consistency checks.
- Brand-fidelity checks.
- Improved incomplete-brief handling.
- Explicit still-image and video modes.
- Consistent response validation.
- Multi-scene planning.
- Platform-independent fallback.
- Acceptance and comparison test documentation.

These features extend rather than replace the original direction workflow.

## Repository layout

    diretor-criativo-ultimate/
    ├── README.md
    ├── LICENSE
    ├── CHANGELOG.md
    └── .agents/
        └── skills/
            └── diretor-criativo-ultimate/
                ├── SKILL.md
                ├── references/
                │   ├── PLATFORM-GUIDE.md
                │   └── EXAMPLES.md
                └── tests/
                    ├── ACCEPTANCE.md
                    └── COMPARISON.md

## Installation

### Project-level installation

Clone the repository into a compatible project's working directory:

    git clone https://github.com/OWNER/diretor-criativo-ultimate.git

Copy the skill directory into the project's Agent Skills discovery location:

    mkdir -p .agents/skills
    cp -R diretor-criativo-ultimate/.agents/skills/diretor-criativo-ultimate .agents/skills/

Alternatively, keep the entire repository in a project whose agent supports discovering the nested skill path.

Replace OWNER with your GitHub username or organization.

### Manual installation

Copy the folder:

    .agents/skills/diretor-criativo-ultimate/

into the corresponding location in your project.

The main file must remain named SKILL.md.

### Client compatibility

An AI agent must support loading Agent Skills or accept the skill instructions through its configured instruction mechanism.

Discovery, automatic activation, file reading, and precedence differ between products.

If the client does not discover `.agents/skills/`, consult its specific skills documentation.

Do not assume that simply copying files guarantees activation in every client.

## Usage

Invoke the skill naturally by requesting cinematic prompt direction.

Examples:

    Create a cinematic prompt for a luxury watch commercial.

    Adapt this scene for Kling 3.0 with believable camera movement.

    Create a Nano Banana Pro editorial product photograph.

    Analyze my attached reference image and write a matching cinematic prompt.

    Refine this cinematic prompt while preserving its subject and lighting.

    Turn the previous prompt into a 10-shot storyboard.

### Default response

The standard output contains:

1. One English cinematic paragraph in a fenced code block.
2. A PARAMS line.
3. An optional storyboard question.

Example:

    ```text
    A solitary runner crosses a rain-soaked city street at dawn...
    ```

    PARAMS — 16:9 | 8 seconds | natural 35mm cinematic perspective

    Would you like a storyboard based on this prompt?

### Storyboard mode

A storyboard is generated only when explicitly requested or confirmed.

The default storyboard contains 8–12 shots organized into acts.

## Example tasks

### Luxury product

    Write a premium Nano Banana Pro prompt for a brushed-steel wristwatch on dark limestone, with controlled studio reflections.

### Human emotion

    Create a Higgsfield scene of a woman processing unexpected good news while sitting beside a train window.

### Dynamic action

    Write a Kling 3.0 video prompt showing a motorcycle moving through a wet tunnel in one continuous shot.

### Atmospheric commercial

    Build a Seedance 2.0 scene for a perfume bottle surrounded by moving silk and soft golden light.

### Reference transformation

    Use the attached image as a reference for lighting and palette, but change the environment to a luxury hotel lobby.

## Tools and permissions

### Required

- A compatible language-model agent.
- Ability to load or receive SKILL.md instructions.

### Optional

- Image understanding for visual references.
- Document-reading capability for written creative briefs.
- External search, if authorized, for additional public research.
- External image/video models for generating actual visual assets.

### Not required

- Image-generation tools.
- Video-generation APIs.
- Paid platform subscriptions.
- Shell access during normal prompt generation.
- Network access for core text operation.
- User credentials.

## Limitations

The skill does not:

- Generate images or videos.
- Edit uploaded images.
- Guarantee visual-model outcomes.
- Guarantee accurate typography or logos in generated media.
- Verify private brand guidelines that have not been supplied.
- Access inaccessible files.
- Control external generation-platform settings.
- Guarantee that suggested durations or aspect ratios are supported.
- Reproduce hidden or unavailable configurations of the original agent.

Platform behavior is expressed as creative guidance rather than verified API syntax.

## Testing

The repository includes:

- `tests/ACCEPTANCE.md`: behavioral acceptance cases.
- `tests/COMPARISON.md`: original-versus-skill test matrix.

Test both systems with identical user requests.

Compare outputs using the same evaluation criteria.

Do not claim full equivalence before running the test suite.

To validate Agent Skills metadata with a compatible validator:

    skills-ref validate .agents/skills/diretor-criativo-ultimate

The command requires a separately installed compatible validation tool.

Reference specification:

https://agentskills.io/specification

## Updating

1. Create a feature branch.
2. Update SKILL.md without removing preserved behavior.
3. Update reference files if necessary.
4. Add tests for every changed behavior.
5. Rerun existing acceptance tests.
6. Compare results against the previous skill version.
7. Document changes in CHANGELOG.md.
8. Increment the version.
9. Publish the tested changes.

Suggested versioning:

- Patch: clarification or corrective changes.
- Minor: backward-compatible creative capabilities.
- Major: changes to core response contracts or operating behavior.

## Publishing

Initialize and publish the repository with GitHub CLI or Git.

Example:

    git init
    git add .
    git commit -m "feat: initial Diretor Criativo Ultimate skill"
    git branch -M main
    gh repo create diretor-criativo-ultimate --public --source=. --remote=origin --push

GitHub CLI authentication must be completed locally.

Never paste tokens or passwords into a chat conversation.

## Licensing

This repository is distributed under the MIT License.

Review ownership and rights to all contributed materials before publication.

## Functional parity status

Status: specification reconstructed; comparative runtime validation pending.

The skill preserves identifiable behavior but does not claim complete equivalence with the original agent.

## Author and attribution

Diretor Criativo™ is the functional identity associated with the reconstructed agent.

Repository ownership, branding rights, and author metadata should be confirmed by the publisher before release.
