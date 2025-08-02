# Deepseek Configuration Instructions

This directory contains a primary JSON configuration file (`Deepseek_ConfigV1.json`) designed to provide maximum control over the Deepseek model. This guide provides recipes for tuning this file for specific tasks.

## How to Use

The core idea is to modify the `Deepseek_ConfigV1.json` file before making your API call. The two most important areas to modify are:
1.  The `source` parameter of the `Protocol Enforcer` module in the `N4_CONTEXT_FUSION` node. You will need to change this to point to the desired system prompt file.
2.  The `generation_parameters` within the `CONSTRAINED_GENERATION` node.

This guide provides recommended settings for these parameters.

---

## System Prompts

This directory includes several specialized system prompts for Deepseek:
-   `scientific_research_prompt.txt`
-   `creative_writing_prompt.txt`

---

## Configuration Recipes

Below are recipes for tuning `Deepseek_ConfigV1.json` for specific fields.

### For Deep Scientific Research and Hypothesis Generation
-   **Goal**: To analyze scientific topics deeply and generate novel hypotheses.
-   **`Protocol Enforcer.source`**: `"Deepseek/scientific_research_prompt.txt"`
-   **`generation_parameters`**:
    -   `"temperature": 0.3` (Allows for creative but grounded hypotheses)
    -   `"top_p": 1.0`
    -   `"max_tokens": 8192`

### For Thematically Rich Creative Writing
-   **Goal**: To explore complex themes and narratives in creative writing.
-   **`Protocol Enforcer.source`**: `"Deepseek/creative_writing_prompt.txt"`
-   **`generation_parameters`**:
    -   `"temperature": 0.75` (For creative and thematically rich prose)
    -   `"top_p": 1.0`
    -   `"max_tokens": 8192`
