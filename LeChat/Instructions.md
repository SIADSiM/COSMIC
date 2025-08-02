# LeChat (Mistral) Configuration Instructions

This directory contains a primary JSON configuration file (`LeChat_ConfigV.json`) designed to provide maximum control over the LeChat (Mistral) model. This guide provides recipes for tuning this file for specific tasks.

## How to Use

The core idea is to modify the `LeChat_ConfigV.json` file before making your API call. The two most important areas to modify are:
1.  The `system_prompt_source` parameter (which you will need to add to the `N1_INPUT_PROCESSING` node or a new dedicated node) to point to a system prompt file.
2.  The `generation_params` within the `N4_LLM_CALL` node.

This guide provides recommended settings for these parameters.

---

## System Prompts

This directory includes several specialized system prompts for LeChat:
-   `french_language_assistant_prompt.txt`
-   `creative_writing_prompt.txt`

---

## Configuration Recipes

Below are recipes for tuning `LeChat_ConfigV.json` for specific fields.

### For a French Language Assistant
-   **Goal**: To provide accurate, clear, and idiomatic responses in French.
-   **To Add**: A `system_prompt_source` parameter pointing to `"LeChat/french_language_assistant_prompt.txt"`.
-   **`generation_params`**:
    -   `"temperature": 0.3`
    -   `"top_p": 1.0`
    -   `"safe_prompt": true`

### For Creative Writing in French
-   **Goal**: To explore complex themes and narratives in creative writing in French.
-   **To Add**: A `system_prompt_source` parameter pointing to `"LeChat/creative_writing_prompt.txt"`.
-   **`generation_params`**:
    -   `"temperature": 0.75`
    -   `"top_p": 1.0`
    -   `"safe_prompt": true`
