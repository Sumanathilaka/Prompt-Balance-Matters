# Prompt Balance Matters: Multilingual Word Sense Disambiguation with Few-Shot Learning

This repository contains the official implementation of the experiments presented in the paper:

**Prompt Balance Matters: Understanding How Imbalanced Few-Shot Learning Affects Multilingual Sense Disambiguation in LLMs**
*Deshan Sumanathilaka, Nicholas Micallef, Julian Hough*
Department of Computer Science, Swansea University, Wales, UK

## 📄 Overview

Recent advances in Large Language Models (LLMs) have opened new possibilities for multilingual Word Sense Disambiguation (WSD). However, few-shot prompting strategies can introduce bias—especially in low-resource languages—when the distribution of senses in prompts is imbalanced.

This project builds upon **GLOSSGPT** and introduces a multilingual WSD setup using **GPT-4o** and **LLaMA-3.1-70B**. We systematically investigate three few-shot sampling strategies:

1. **Highest Frequency Sharing** – Favors the most common sense.
2. **Lowest Frequency Sharing** – Equalizes examples using the least frequent sense.
3. **Average Frequency Sharing** – Balances between the highest and lowest frequencies.

Our findings show:

* Balanced prompting is crucial for reducing bias in multilingual WSD.
* The optimal strategy depends on the target language and the model.
* Under-resourced languages are especially sensitive to frequency imbalance.

---

## 📊 Datasets

We use the **SemEval-2013 WSD dataset** for English, German, Spanish, French, and Italian.

* **300 samples per language** (each with one ambiguous word)
* Lexical knowledge sourced from **BabelNet** and **WordNet**
* Data preprocessed to ensure each word has at least two distinct senses

---



## 📌 Citation

If you use this code, please cite:

```
@inproceedings{sumanathilaka2025promptbalance,
  title={Prompt Balance Matters: Understanding How Imbalanced Few-Shot Learning Affects Multilingual Sense Disambiguation in LLMs},
  author={Sumanathilaka, Deshan and Micallef, Nicholas and Hough, Julian},
  year={2025},
  booktitle={Proceedings of GlobalNLP 2025}
}
```

---

## ⚠️ Limitations

* Only tested on GPT-4o and LLaMA-3.1-70B
* Dataset limited to 300 samples per language due to BabelNet API constraints
* Models are general-purpose; results may differ with reasoning-specialised LLMs

---

## 📬 Contact

For questions, please contact:
**Deshan Sumanathilaka** – [t.g.d.sumanathilaka@swansea.ac.uk](mailto:t.g.d.sumanathilaka@swansea.ac.uk)


If you’d like, I can also create a **shorter, cleaner “user-friendly” README** for public release while keeping this detailed one for research use. That could help balance technical completeness with broader readability. Would you like me to do that?
