# Appendix W: LLM Security

## Introduction

The popularity of Large Language Models (LLM) like GPT variants from OpenAI has been on a rise, giving applications the power to generate human-like text based on prompts. However, this has opened up many potential vulnerabilities.

While this topic is not the core competency of the ASVS, we wanted to include some basic guidelines as an appendix in the hope that a more comprehensive verification standard will be prepared for LLMs and AI in general in the future.

These have not gone undergone the same rigourous review and discussion as the main ASVS requirements so should be used with caution.

## W.1 Input Validation and Sanitization

Ensure that all inputs to the LLM are properly validated and sanitized to prevent injection attacks and other malicious inputs.

| # | Description | L1 | L2 | L3 | CWE |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **W.1.1** | Verify that all inputs to the LLM are validated for expected data types, lengths, and formats. | ✓ | ✓ | ✓ | 20 |
| **W.1.2** | Verify that inputs are sanitized to remove potentially harmful content before processing by the LLM. | ✓ | ✓ | ✓ | 116 |
| **W.1.3** | Verify that a dedicated AI system, which does not contain sensitive data, is used to validate natural language questions for security before processing by the LLM. | ✓ | ✓ | ✓ | 924 |

## W.2 Output Filtering

Ensure that the outputs generated by the LLM are filtered and sanitized to prevent the disclosure of sensitive information and to avoid generating harmful content.

| # | Description | L1 | L2 | L3 | CWE |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **W.2.1** | Verify that outputs from the LLM are reviewed and filtered to prevent the leakage of sensitive data. | ✓ | ✓ | ✓ | 200 |
| **W.2.2** | Verify that outputs are sanitized to avoid generating harmful or inappropriate content. | ✓ | ✓ | ✓ | 89 |

## W.3 Access Control and Authentication

Ensure that access to the LLM and its functionalities is properly controlled and authenticated to prevent unauthorized use.

| # | Description | L1 | L2 | L3 | CWE |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **W.3.1** | Verify that access to the LLM is restricted to authenticated and authorized users only. | ✓ | ✓ | ✓ | 287 |
| **W.3.2** | Verify that strong authentication mechanisms are in place for accessing the LLM. | ✓ | ✓ | ✓ | 307 |
