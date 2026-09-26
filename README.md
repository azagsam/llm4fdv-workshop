# AI4SS: Workshop for Social Sciences

A practical introduction to large language models for social science researchers with basic Python experience: coding open-ended survey responses, analysing interview transcripts, classifying media and political texts, working with multilingual data.

The emphasis throughout is on the questions that matter empirically — how reliable model outputs are, how to validate them, and how to make the analysis reproducible.

## Preparing the environment

Check the instructions you received by mail. Dependencies are listed in `resources/requirements.txt`; notebooks also install what they need when run on Colab or Kaggle.

## Repository structure

| Folder | Contents |
|---|---|
| `demos/` | Walked through together during the session |
| `exercises/` | Individual work — starter code with `TODO`s, one per demo; worked solutions with sample answers in `exercises/solutions/` |
| `projects/` | Two 2-hour team projects, data loaded from Hugging Face; instructor solutions in `projects/solutions/` |
| `supplementary/` | Optional background: ML basics, word2vec, text classification |
| `resources/` | Environment setup |

### Demos

| Notebook | Topic |
|---|---|
| `Minimal_openai_and_embeddings` | A hosted chat model via the OpenAI API, and embeddings computed locally |
| `Basics_of_text_generation` | How decoding parameters (temperature, top-k/p, beam search) shape the output |
| `Prompting_LLMs` | Zero-shot, few-shot, system prompts, chain-of-thought, ReAct |
| `Retrieval_augmented_generation` | Grounding answers in your own documents, built from scratch |

Each exercise mirrors the demo of the same name and treats the technique as a **research instrument**: it measures how far the undocumented choices — decoding parameters, prompt wording, chunk size — move the numbers you would report.

### Projects

- **Interview coding** — an LLM as second coder for 1,250 qualitative interviews about AI at work. Codebook design, structured output, quote verification, agreement with a blind human coder (Cohen's kappa), group comparison. Also available as `Project_1_Interview_coding_open_models.ipynb`, which runs an open-weight model (Qwen2.5-3B-Instruct) on a local GPU instead of the OpenAI API.
- **Parliamentary framing** — how left and right MPs frame issues in Slovenian parliamentary speeches. Validation against a known label, the Policy Frames Codebook, repeated coding for stability, blind human check.
