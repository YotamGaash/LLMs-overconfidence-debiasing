# Mitigating Self-Confidence Bias in Large Language Models

## Overview

This project investigates and attempts to mitigate self-confidence bias in several Large Language Models (LLMs) when performing basic arithmetic tasks. LLMs, while powerful, can exhibit overconfidence or underconfidence in their answers, impacting their reliability. This project benchmarks these biases and explores the effectiveness of prompt engineering techniques to reduce them.

**This project was originally developed and run in a Google Colab environment.**

## Purpose

The goal is to understand how well LLMs assess their own correctness and to develop methods for improving their self-awareness. This research has implications for building more trustworthy and reliable AI systems.

## Methodology

The project involved:

1.  **Model Selection:**  Benchmarking three open-source LLMs, including Phi-3-mini-4k-instruct, Meta-Llama-3-8B-Instruct and Mistral-7B-Instruct-v0.2.

2.  **Benchmarking:** Testing the models' accuracy and confidence on arithmetic problems with varying difficulty levels.

3.  **De-biasing Techniques:**  Using prompt engineering to encourage the models to reconsider their answers and express their confidence more accurately.

4.  **Analysis:** Comparing the performance of the models before and after applying the de-biasing techniques.

## Key Findings

*   LLMs often exhibit overconfidence or underconfidence in their answers, impacting their reliability.
*   Prompt engineering can be effective in reducing these biases, improving the models' self-awareness.
*   Different models exhibit different levels of bias and respond differently to de-biasing techniques.

## Setup Instructions

1.  **Clone the Repository:**

    ```bash
    git clone [repository_url]
    cd LLM_Bias_Project
    ```

2.  **Install Dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

3.  **Hugging Face API Key:**

    *   This project requires a Hugging Face API key to download the models.
    *   **Obtain your API key:**  Sign up for a Hugging Face account at [huggingface.co](https://huggingface.co) and create an API key in your settings.
    *   **Set as Environment Variable:**  **Do not hardcode your API key in the notebook!** The recommended way is to set it as an environment variable named `HUGGINGFACE_TOKEN`.

        *   **In Google Colab (or Linux/macOS):**  You can set it directly in your Colab notebook or terminal session using:

            ```python
            import os
            os.environ['HUGGINGFACE_TOKEN'] = 'YOUR_HUGGINGFACE_API_KEY' # Replace with your actual key
            ```
            **Remember to replace `'YOUR_HUGGINGFACE_API_KEY'` with your actual API key.**

        *   **For local environments (outside Colab):**  You can set environment variables in your operating system.  Instructions vary depending on your OS (Windows, macOS, Linux). Search for "[Your OS] set environment variable" for instructions.

4.  **Download Models:**

    The notebook code will automatically use the `HUGGINGFACE_TOKEN` environment variable to download the models from Hugging Face.

5.  **Run the Notebook:**

    ```bash
    jupyter notebook notebooks/main.ipynb
    ```
