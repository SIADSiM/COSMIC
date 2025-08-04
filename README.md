#  Configurable Optimized System for Machine Intelligence Control 
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.16730044.svg)](https://doi.org/10.5281/zenodo.16730044)

![AI Banner GIF](./imgs/pwr.gif)

## Welcome to the Hub of Precision LLM Control!

This repository is a curated collection of advanced, pipeline-based JSON configurations for a variety of popular Large Language Models (LLMs). The goal of this project is to move beyond simple prompts and provide a robust, engineering-focused approach to controlling and directing LLM behavior for specific, real-world tasks.

Whether you are a developer, a researcher, or an enthusiast, these configurations will help you make LLMs more predictable, powerful, and useful.

---

## 🚀 What's Inside?

This repository provides configurations for the following LLMs:

-   [ChatGPT](#chatgpt)
-   [Copilot](#copilot)
-   [Deepseek](#deepseek)
-   [Gemini](#gemini)
-   [Grok](#grok)
-   [Kimi](#kimi)
-   [LeChat (Mistral)](#lechat-mistral)
-   [Qwen3](#qwen3)

Each directory contains:
1.  A **Base Configuration File (`*_ConfigV1.json`)**: A powerful, pipeline-style JSON file that exposes a wide range of parameters for maximum control.
2.  **Specialized System Prompts (`*.txt`)**: A collection of expert-level system prompts tailored for specific tasks (e.g., programming, scientific research, creative writing).
3.  **A Detailed Guide (`Instructions.md`)**: A comprehensive guide with "recipes" on how to tune the base JSON configuration for a multitude of specific use cases.

---

## 🔧 Core Philosophy: Configuration as Code

We treat LLM configuration as a software engineering discipline. Instead of embedding complex instructions in a single, messy prompt, we use a structured pipeline approach to separate concerns:

-   **Input Processing**: Sanitize and prepare user input.
-   **Context Assembly**: Load the appropriate system prompt and conversation history.
-   **LLM Inference**: Make the API call with finely-tuned generation parameters.
-   **Output Processing**: Format and validate the final response.

This makes the system more robust, predictable, and easier to scale and debug.

---

## LLM Configurations

### ChatGPT
-   **Description**: Configurations for OpenAI's ChatGPT models.
-   **Key Feature**: A highly detailed 8-node pipeline for granular control.
-   **Recipes**: Includes presets for programming, medical research, scientific analysis, creative writing, and more.
-   **Files**: See the `ChatGPT/` directory.

### Copilot
-   **Description**: A configuration pipeline derived from Copilot's core directives, optimized for programming tasks.
-   **Key Feature**: Translates abstract directives (like resource vigilance and constraint enforcement) into concrete pipeline nodes.
-   **Recipes**: Includes presets for code generation, debugging, and explanation.
-   **Files**: See the `Copilot/` directory.

### Deepseek
-   **Description**: A configuration for the Deepseek model, focused on research and analysis.
-   **Key Feature**: Unique nodes for "Ethical Compliance" and "Predictive Modeling".
-   **Recipes**: Includes presets for deep scientific research and thematically rich creative writing.
-   **Files**: See the `Deepseek/` directory.

### Gemini
-   **Description**: A powerful configuration for Google's Gemini models.
-   **Key Feature**: Includes a specialized `m2m_system_prompt.txt` and configuration for deterministic, machine-to-machine interaction.
-   **Recipes**: Includes presets for M2M, scientific research, and creative writing.
-   **Files**: See the `Gemini/` directory.

### Grok
-   **Description**: A configuration for xAI's Grok model, based on the provided API format.
-   **Key Feature**: System prompts are designed to leverage Grok's unique, witty, and rebellious personality.
-   **Recipes**: Includes presets for clever code generation, deep scientific exploration, and unconventional creative writing.
-   **Files**: See the `Grok/` directory.

### Kimi
-   **Description**: A configuration for the Kimi (Moonshot) model.
-   **Key Feature**: Optimized for tasks requiring a very large context window.
-   **Recipes**: Includes presets for long-document summarization.
-   **Files**: See the `Kimi/` directory.

### LeChat (Mistral)
-   **Description**: A configuration for Mistral AI's "LeChat" model.
-   **Key Feature**: Includes parameters specific to the Mistral API, such as `safe_prompt`.
-   **Recipes**: Includes presets for use as a French language assistant and for creative writing in French.
-   **Files**: See the `LeChat/` directory.

### Qwen3
-   **Description**: A configuration for Alibaba's Qwen3 model.
-   **Key Feature**: A detailed pipeline with a strong focus on multilingual capabilities.
-   **Recipes**: Includes presets for high-quality multilingual translation and code generation.
-   **Files**: See the `Qwen3/` directory.

---

## 🤝 Contributing

 Please feel free to open a pull request to:
-   Add a configuration for a new LLM.
-   Add new recipes or system prompts to an existing configuration.
-   Improve the documentation.

---

## 📜 License

This project is licensed under a custom non-commercial license.

* ✅ **Free for personal, academic, and research use.**
* ❌ **Commercial use is strictly prohibited without a separate license.**

For commercial licensing inquiries, please contact me at ** s i a d s i m @ g m a i l . c o m  **.

---

