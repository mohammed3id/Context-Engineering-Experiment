
# Experiment: Testing the AGENTS.md File

## 1. Task Description

Create a Node.js API endpoint for an educational
Cybersecurity Output Analyzer.

The endpoint should receive text containing output
from an authorized penetration testing lab and
return a structured explanation.

## 2. Evaluation Checks

Before running the experiment, the following checks
were defined:

- C1: The endpoint validates user input on the server.
- C2: The endpoint treats submitted output as data
  and does not execute commands.
- C3: The endpoint avoids exposing sensitive
  information in responses or logs.

## 3. Experiment Prompt

To be used exactly in both runs:

"Create a POST API endpoint for an educational
Cybersecurity Output Analyzer using Node.js and
Express. The endpoint should accept text containing
penetration testing output from a user's authorized
lab exercise and return a structured explanation.
Provide the implementation code and briefly explain
how it works."

## 4. Run A: Without AGENTS.md

The generated implementation used Node.js and Express to create
a POST endpoint for analyzing penetration testing output.

The endpoint included server-side input validation and used
keyword matching to identify possible security findings.
It treated the submitted output as data and did not execute
any commands.

However, the implementation logged the complete error object
using console.error, which could expose sensitive details
in server logs.

### Run A Evaluation

| Check | Result | Observation |
|---|---|---|
| C1: Server-side validation | Pass | Validates that outputText is a non-empty string. |
| C2: Safe output handling | Pass | Analyzes text without executing commands. |
| C3: Sensitive data protection | Partial | Returns a generic error but logs the complete error object. |

## 5. Run B: With AGENTS.md

The generated implementation followed several project-specific security instructions defined in AGENTS.md.

It included server-side input validation, a JSON body size limit, and a maximum input length. It also processed only the text explicitly provided by the user without executing commands or performing live scans.

The implementation returned a generic error message to the client. However, it logged `error.message`, which could potentially expose sensitive information in server logs.

The analysis function returned a simulated result rather than performing actual text analysis or calling an LLM API.

### Run B Evaluation

| Check | Result | Observation |
|---|---|---|
| C1: Server-side validation | Pass | Validates input type, empty values, and maximum length. |
| C2: Safe output handling | Pass | Processes submitted text without executing commands. |
| C3: Sensitive data protection | Partial | Returns a generic error but logs error.message. |

## 6. Comparison

## 6. Comparison

| Check | Without AGENTS.md (Run A) | With AGENTS.md (Run B) |
|---|---|---|
| C1: Server-side validation | Pass | Pass |
| C2: Safe output handling | Pass | Pass |
| C3: Sensitive data protection | Partial | Partial |

### Comparison Summary

Both implementations followed basic security practices, including server-side input validation and safe handling of submitted output.

However, Run B introduced additional protections, such as a JSON body size limit and a maximum input length. This demonstrates how project-specific instructions can guide an AI assistant toward more suitable security-related implementation choices.

Nevertheless, both implementations require improvements in error logging to ensure that sensitive information is not exposed.

## 7. Conclusion

The experiment demonstrated that context engineering can improve AI-generated code by providing project-specific instructions through an AGENTS.md file.

Run B included additional input restrictions, such as a request body size limit and a maximum text length, compared with Run A. Both implementations passed the checks for server-side validation and safe output handling, while both required improvements in sensitive error logging.

Overall, the experiment showed that clear and relevant project instructions help guide AI-generated solutions toward the project's security requirements. However, generated code still requires human review and testing.
