# cybersecurity-learning-platform
AI-assisted cybersecurity learning platform - Context Engineering experiment Visibility

# Context Engineering Experiment
### AI Fluency – Week 4

## About This Repository

This repository contains a practical experiment exploring Context Engineering and its impact on AI-generated code.

The experiment investigates how providing an AI assistant with structured project instructions through an `AGENTS.md` file can influence the quality, consistency, and security of its generated solutions.

## Experiment Overview

The experiment consists of two runs:

- **Run A – Without Context:** The AI assistant receives a development task without any additional project-specific instructions.
- **Run B – With Context:** The AI assistant receives the same development task after being provided with an `AGENTS.md` file containing project context and specific instructions.

The generated outputs are then compared to evaluate the effect of context engineering.

## Evaluation Criteria

The experiment evaluates the generated implementations using three criteria:

1. Server-side input validation.
2. Safe handling of user-provided data.
3. Protection of sensitive information.

## Repository Contents

| File | Description |
|---|---|
| `AGENTS.md` | Contains the project context, security rules, and coding instructions. |
| `REMOVAL_TEST.md` | Examines the importance of retaining critical instructions. |
| `OMISSIONS.md` | Explains three deliberately excluded instructions and the reasons for excluding them. |
| `EXPERIMENT.md` | Documents both experimental runs, their evaluation, and the comparison. |

## Key Learning Outcome

This experiment demonstrates how structured context and clear instructions can guide AI assistants toward generating solutions that better match specific project requirements.

It also highlights the importance of reviewing and evaluating AI-generated code rather than relying on it without verification.

## Purpose

This repository was created as part of an AI Fluency internship task focused on Context Engineering.
