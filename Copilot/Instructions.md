# Copilot Configuration Instructions

This directory contains a primary JSON configuration file (`Copilot_ConfigV1.json`) designed to provide maximum control over the Copilot model for programming tasks. This guide provides recipes for tuning this file for specific use cases.

## How to Use

The core idea is to modify the `Copilot_ConfigV1.json` file before making your API call. The two most important areas to modify are:
1.  The `system_prompt_source` parameter in the `N4_CONTEXT_ASSEMBLY` node (Note: You will need to add this parameter to the config, as the base config uses a hardcoded system prompt).
2.  The `generation_params` within the `N5_LLM_EXECUTION` node.

This guide provides recommended settings for these parameters.

---

## System Prompts

This directory includes several specialized system prompts for programming tasks:
-   `code_generation_prompt.txt`
-   `code_debugging_prompt.txt`
-   `code_explanation_prompt.txt`

---

## Configuration Recipes

Below are recipes for tuning `Copilot_ConfigV1.json` for specific fields.

### For High-Quality Code Generation
-   **Goal**: Produce clean, efficient, and production-ready code.
-   **To Add**: Modify the `N4_CONTEXT_ASSEMBLY` node to include a `system_prompt_source` parameter and point it to `"Copilot/code_generation_prompt.txt"`.
-   **`generation_params`**:
    -   `"temperature": 0.1`
    -   `"top_p": 1.0`
    -   `"max_tokens": 8192`

### For Precise Code Debugging
-   **Goal**: Analyze existing code and provide accurate debugging help.
-   **To Add**: Modify the `N4_CONTEXT_ASSEMBLY` node to include a `system_prompt_source` parameter and point it to `"Copilot/code_debugging_prompt.txt"`.
-   **`generation_params`**:
    -   `"temperature": 0.0` (For deterministic analysis)
    -   `"top_p": 1.0`

### For Clear Code Explanation
-   **Goal**: Explain code in a way that is easy to understand.
-   **To Add**: Modify the `N4_CONTEXT_ASSEMBLY` node to include a `system_prompt_source` parameter and point it to `"Copilot/code_explanation_prompt.txt"`.
-   **`generation_params`**:
    -   `"temperature": 0.3` (Factual but with fluid, natural language)
    -   `"top_p": 1.0`
