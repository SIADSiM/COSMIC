# Gemini Configuration Instructions

This directory contains a primary JSON configuration file (`Gemini_ConfigV1.json`) designed to provide maximum control over the Gemini model. This guide provides recipes for tuning this file for specific tasks.

## How to Use

The core idea is to modify the `Gemini_ConfigV1.json` file before making your API call. The two most important areas to modify are:
1.  The `system_prompt_source_path` parameter in the `N4_CONTEXT` node.
2.  The `inference_parameters` within the `N6_LLM_INFERENCE` node.

This guide provides recommended settings for these parameters.

---

## System Prompts

This directory includes several specialized system prompts for Gemini:
-   `m2m_system_prompt.txt`
-   `scientific_research_prompt.txt`
-   `creative_writing_prompt.txt`

---

## Configuration Recipes

Below are recipes for tuning `Gemini_ConfigV1.json` for specific fields.

### For Machine-to-Machine (M2M) Interaction
-   **Goal**: To force Gemini to behave as a deterministic, instruction-following machine.
-   **`system_prompt_source_path`**: `"Gemini/m2m_system_prompt.txt"`
-   **`inference_parameters`**:
    -   `"temperature": 0.0`
    -   `"top_k": 1`
    -   `"seed": 42`

### For Deep Scientific Research
-   **Goal**: To analyze scientific topics deeply and generate novel hypotheses.
-   **`system_prompt_source_path`**: `"Gemini/scientific_research_prompt.txt"`
-   **`inference_parameters`**:
    -   `"temperature": 0.3`
    -   `"top_k": 40`

### For Thematically Rich Creative Writing
-   **Goal**: To explore complex themes and narratives in creative writing.
-   **`system_prompt_source_path`**: `"Gemini/creative_writing_prompt.txt"`
-   **`inference_parameters`**:
    -   `"temperature": 0.75`
    -   `"top_k": 50`
