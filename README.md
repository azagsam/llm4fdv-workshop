# LLM4FDV: Workshop for Social Sciences

A practical introduction to large language models for social science researchers with basic Python experience: generating text with open models, prompting, retrieval-augmented generation, and using an LLM as a coder for qualitative data.

The emphasis throughout is on the questions that matter empirically — how reliable model outputs are, how to validate them, and how to make the analysis reproducible.

## Preparing the environment

Check the instructions you received by mail. 

## Repository structure

| Folder | Contents |
|---|---|
| `demos/` | Walked through together during the session |
| `exercises/` | Individual work: starter code with `# <-- FIX` / `# TODO` markers` |
| `project/` | A 2-hour hands-on project |

### Demos

| Notebook | Topic |
|---|---|
| `OpenAI` | A hosted chat model via the `openai` library: chat completion, JSON output, comparing texts with embeddings |
| `Basics_of_text_generation` | How decoding parameters (length, temperature, top-k/p, repetition penalties, beam search) shape the output; stopping, streaming, reproducibility, reasoning models |
| `Prompting_LLMs` | Chat templates, zero-shot, few-shot, system prompts, chain-of-thought, structured output |
| `Retrieval_augmented_generation` | Grounding answers in your own documents, built from scratch: chunking, embedding search, prompting, evaluating retrieval and groundedness |

### Exercises

**Generation parameters and prompting warm-up** — 15 short exercises following the *Basics of text generation* and *Prompting LLMs* demos. Each gives a goal and code that does not reach it yet (a parameter missing or mis-set, or an unclear prompt); you fix it and check the result.

- Part A (1–10): generation parameters — truncated answers, unstable labels, gibberish, identical samples, reproducible sampling.
- Part B (11–15): prompting — label-only answers, system prompts, few-shot examples, chain-of-thought, valid JSON.

### Project

**Interview coding** — an LLM as a coder for the 1,250 interviews about AI at work in [`Anthropic/AnthropicInterviewer`](https://huggingface.co/datasets/Anthropic/AnthropicInterviewer) (general workforce, creatives, scientists). Research question: do the three occupational groups differ in their attitude towards AI and in what worries them most?

Steps: read the data, adapt the codebook, write the prompt and code one interview, code the whole sample, add a second coder from a different model family and measure agreement (Cohen's kappa), and answer the substantive question (chi-square test).

No Python writing is needed — every `TODO` is a research decision (a prompt, a setting, a model). The notebook runs an open-weight model (Qwen2.5-3B-Instruct by default) locally, so no API key is needed and no interview text leaves your machine.
