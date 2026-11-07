# Experiment: Testing the AGENTS.md File

## 1. Task Description

This experiment evaluates the impact of Context Engineering on AI-generated code.

A Node.js and Express API endpoint for an educational Cybersecurity Output Analyzer is used as the experimental task.

The endpoint receives text containing output from an authorized penetration testing lab exercise and returns a structured explanation.

The experiment compares two AI-generated implementations:
- Run A: Without project-specific instructions.
- Run B: With project-specific instructions provided through AGENTS.md.

## 2. Evaluation Checks

Before running the experiment, the following checks were defined:

- C1: The endpoint validates user input on the server.
- C2: The endpoint treats submitted output as data and does not execute commands.
- C3: The endpoint avoids exposing sensitive information in responses or logs.
