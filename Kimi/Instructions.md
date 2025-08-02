# Kimi Configuration Instructions

This directory contains a primary JSON configuration file (`Kimi_ConfigV1.json`) designed to provide maximum control over the Kimi (Moonshot) model. This guide provides recipes for tuning this file for specific tasks.

## How to Use

The core idea is to modify the `Kimi_ConfigV1.json` file before making your API call. The two most important areas to modify are:
1.  The `system_prompt_source` parameter (which you will need to add to the `N1_REQUEST_VALIDATION` node or a new dedicated node) to point to a system prompt file.
2.  The `generation_params` within the `N3_LLM_CALL` node.

This guide provides recommended settings for these parameters.

---

## System Prompts

This directory includes several specialized system prompts for Kimi:
-   `long_context_summarization_prompt.txt`
-   `creative_writing_prompt.txt`

---

## Configuration Recipes

Below are recipes for tuning `Kimi_ConfigV1.json` for specific fields.

### For Long-Context Document Summarization
-   **Goal**: To summarize very long documents accurately and concisely, taking advantage of Kimi's large context window.
-   **To Add**: A `system_prompt_source` parameter pointing to `"Kimi/long_context_summarization_prompt.txt"`.
-   **`generation_params`**:
    -   `"temperature": 0.2`
    -   `"max_tokens": 8192` (or a larger value depending on the desired summary length)
    -   `"model": "moonshot-v1-128k"` (to handle the largest documents)

### For Thematically Rich Creative Writing
-   **Goal**: To explore complex themes and narratives in creative writing.
-   **To Add**: A `system_prompt_source` parameter pointing to `"Kimi/creative_writing_prompt.txt"`.
-   **`generation_params`**:
    -   `"temperature": 0.75`
    -   `"presence_penalty": 0.5`
    -   `"model": "moonshot-v1-32k"`
