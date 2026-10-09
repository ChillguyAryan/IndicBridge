# IndicBridge

**Bidirectional English–Indic Translation using Qwen3-1.7B-Base**

IndicBridge explores multilingual machine translation by fine-tuning **Qwen3-1.7B-Base** for translation between English and Gujarati, Hindi, and Marathi.

## Project Details

- **Base Model:** Qwen3-1.7B-Base
- **Dataset:** AI4Bharat BPCC
- **Languages:** English, Gujarati, Hindi, Marathi
- **Translation Directions:** 6
- **Training Data:** 249,600 sentence pairs
- **Evaluation Benchmarks:** IN22-Gen and IN22-Conv
- **Evaluation Metrics:** BLEU and chrF++

## Translation Directions

| Source | Target |
|---|---|
| English | Gujarati |
| Gujarati | English |
| English | Hindi |
| Hindi | English |
| English | Marathi |
| Marathi | English |

## Methodology

The notebook implements a workflow for multilingual translation:

1. **Data Preparation:** Load, filter, and select parallel text data across six translation directions.
2. **Model Fine-Tuning:** Adapt the pretrained Qwen3-1.7B-Base model using selective parameter fine-tuning.
3. **Training:** Apply target-only cross-entropy loss, token-normalized gradient accumulation, and checkpoint recovery.
4. **Translation Generation:** Generate translations for the evaluation datasets.
5. **Evaluation:** Measure translation quality on IN22-Gen and IN22-Conv using BLEU and chrF++.

## Notebook

The main experiment is implemented in `p1-qwen3-indic-translator.ipynb`.

The notebook contains data preparation, model configuration, fine-tuning, translation generation, and benchmark evaluation.
