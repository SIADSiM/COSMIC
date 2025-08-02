# Qwen3 Configuration Instructions

This directory contains a primary JSON configuration file (`Qwen3_ConfigV1.json`) designed to provide maximum control over the Qwen3 model. This guide provides recipes for tuning this file for specific tasks.

## How to Use

The core idea is to modify the `Qwen3_ConfigV1.json` file before making your API call. The two most important areas to modify are:
1.  The `system_prompt_template` parameter in the `N4_CONTEXT_MANAGER` node.
2.  The `generation_params` within the `N6_LLM_GENERATION` node.

This guide provides recommended settings for these parameters.

---

## System Prompts

This directory includes several specialized system prompts for Qwen3:
-   `multilingual_translator_prompt.txt`
-   `code_generation_prompt.txt`

---

## Configuration Recipes

Below are recipes for tuning `Qwen3_ConfigV1.json` for specific fields.

### For High-Quality Multilingual Translation
-   **Goal**: To accurately translate text between any two languages.
-   **`system_prompt_template`**: `"Qwen3/multilingual_translator_prompt.txt"`
-   **`generation_params`**:
    -   `"temperature": 0.1`
    -   `"top_p": 1.0`
    -   `"repetition_penalty": 1.1`

### For High-Quality Code Generation
-   **Goal**: Produce clean, efficient, and production-ready code.
-   **`system_prompt_template`**: `"Qwen3/code_generation_prompt.txt"`
-   **`generation_params`**:
    -   `"temperature": 0.1`
    -   `"top_p": 1.0`
    -   `"repetition_penalty": 1.05`
