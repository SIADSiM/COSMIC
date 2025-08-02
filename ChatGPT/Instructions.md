# ChatGPT Configuration Instructions

This directory contains several JSON configuration files designed to control the behavior of the ChatGPT model for specific tasks. By using these configurations, you can tune the model to be a specialized tool for programming, medical research, scientific inquiry, or creative writing.

## How to Use

To use these configurations, you would typically have a script or application that reads the desired JSON file and uses its contents to construct the API request to the OpenAI/ChatGPT endpoint. The key is to load the specified `system_prompt_source` and use the `generation` parameters in your API call.

---

## Configuration Files

### 1. `ChatGPT_ConfigV1.json` (Base Configuration)
-   **Purpose**: A general-purpose, enhanced configuration with a full set of parameters for powerful, controlled interaction. It's a good starting point for building your own custom configurations.
-   **Key Settings**:
    -   Full 8-node pipeline for detailed control.
    -   A balanced set of generation parameters.
    -   External lookup enabled by default.

### 2. `ChatGPT_Programming_V1.json`
-   **Purpose**: Optimized for coding tasks, including generation, debugging, and explanation.
-   **System Prompt**: `programming_system_prompt.txt` - Instructs the model to be a precise and accurate programming expert.
-   **Key Settings**:
    -   `temperature: 0.1` for deterministic and accurate code.
    -   Higher penalty parameters to discourage repetitive code.

### 3. `ChatGPT_Medical_V1.json`
-   **Purpose**: Tuned for providing accurate and evidence-based medical information for research purposes. **This is not a substitute for professional medical advice.**
-   **System Prompt**: `medical_system_prompt.txt` - Enforces strict rules about not giving advice and citing sources.
-   **Key Settings**:
    -   `temperature: 0.0` for maximum factual accuracy.
    -   `external_lookup` is enabled and set to `PubMed` to encourage source-based answers.

### 4. `ChatGPT_Scientific_V1.json`
-   **Purpose**: Designed for objective and precise scientific research and explanation.
-   **System Prompt**: `scientific_system_prompt.txt` - Instructs the model to be objective, cite sources, and use precise language.
-   **Key Settings**:
    -   `temperature: 0.1` for factual and objective responses.
    -   `external_lookup` is enabled and set to `ArXiv` to facilitate literature research.

### 5. `ChatGPT_Creative_Writing_V1.json`
-   **Purpose**: Optimized for creative tasks like storytelling, poetry, and brainstorming.
-   **System Prompt**: `creative_writing_system_prompt.txt` - Encourages the model to be an imaginative and collaborative creative partner.
-   **Key Settings**:
    -   `temperature: 0.8` to encourage originality and creativity.
    -   `presence_penalty` is increased to help the model explore new ideas and avoid repetition.

---

By selecting the appropriate configuration file for your task, you can ensure that the model's persona, instructions, and generation style are perfectly aligned with your goals.
