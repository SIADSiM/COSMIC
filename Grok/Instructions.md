# Grok Configuration Instructions

This directory contains a primary JSON configuration file (`Grok_ConfigV1.json`) designed to provide maximum control over the Grok model. This guide provides recipes for tuning this file for specific tasks, leveraging Grok's unique personality.

## How to Use

Modify the `Grok_ConfigV1.json` file before making your API call. The two most important areas to modify are:
1.  The `system_prompt_source` parameter in the `N1_REQUEST_SETUP` node.
2.  The `generation_params` within the `N2_LLM_CALL` node.

This guide provides recommended settings for these parameters.

---

## System Prompts

This directory includes several specialized system prompts tailored for Grok's style:
-   `programming_system_prompt.txt`
-   `scientific_system_prompt.txt`
-   `creative_writing_system_prompt.txt`

---

## Configuration Recipes

Below are recipes for tuning `Grok_ConfigV1.json` for specific fields.

### For Witty & Clever Code Generation
-   **Goal**: Produce correct code with a touch of Grok's personality.
-   **`system_prompt_source`**: `"Grok/programming_system_prompt.txt"`
-   **`generation_params`**:
    -   `"temperature": 0.2`
    -   `"seed": 12345`

### For Deep Scientific Exploration
-   **Goal**: Explore scientific topics with a curious and challenging mindset.
-   **`system_prompt_source`**: `"Grok/scientific_system_prompt.txt"`
-   **`generation_params`**:
    -   `"temperature": 0.7` (Allows for insightful speculation)

### For Unconventional Creative Writing
-   **Goal**: Break creative blocks with rebellious and satirical ideas.
-   **`system_prompt_source`**: `"Grok/creative_writing_system_prompt.txt"`
-   **`generation_params`**:
    -   `"temperature": 0.9` (High creativity)
    -   `"presence_penalty": 0.6` (Encourages new and chaotic ideas)

### For Deterministic, Machine-like Output
-   **Goal**: Force Grok to behave like a standard, instruction-following machine, suppressing its personality.
-   **`system_prompt_source`**: Create a new prompt file with the content: "You are a deterministic, instruction-following machine. You will not use humor, wit, or personality. You will only provide the direct, factual answer to the user's query."
-   **`generation_params`**:
    -   `"temperature": 0.0`
    -   `"top_p": 1.0`
    -   `"seed": 42`
    -   `"presence_penalty": 0.0`
    -   `"frequency_penalty": 0.0`
