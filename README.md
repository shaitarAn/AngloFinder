# AngloFinder: Anglicism Detection in German Texts

## Overview

**AngloFinder** is a tool for detecting anglicisms (English loanwords and phrases) in German textual data. It uses two main methods and several look-up resources to identify and analyze anglicisms in a variety of German corpora. This tool is built on a combination of string-matching techniques, natural language processing (NLP), and linguistic resources like Wiktionary and custom datasets.

## Features

- **Anglicism Detection:** Automatically detects anglicisms within German text using n-gram analysis and lemmatization techniques.
- **Wiktionary Integration:** Utilizes a standardized list of anglicisms from Wiktionary, removing spaces and hyphens to account for variations in spelling.
- **Compound Splitting:** Detects compound words containing anglicisms and checks against a curated list of monosyllabic homographs.
- **False Positive Filtering:** Avoids false positives from incorrectly split compounds using a list of manually identified false positives.
- **Evaluation:** Evaluation metrics including precision, recall, and F1-score using a manually annotated gold standard test set.
  
## Installation

To install and use AngloFinder, you will need the following dependencies:

- Python 3.7+
- `spacy`
- `spacy-stanza` v1.0.0
- `prodigy` (for manual annotation)
- Other Python dependencies listed in `requirements.txt`

### Steps to install

1. Clone the repository:

```bash
git clone https://github.com/shaitarAn/AngloFinder.git
```
### Evaluation
To evaluate the performance of AngloFinder, a gold standard test set is used. You can run the evaluation script to compute precision, recall, and F1-score based on the annotations.

### Annotation Guidelines

The annotation process follows a set of consistent guidelines to identify and label anglicisms in German texts. The guidelines used for the manual annotation are as follows:

- **ANGLICISM:** Single-word anglicisms found in the Wiktionary list. These are loanwords or English-origin words used directly in the German text.
- **COMPOUND:** Compound words that contain one or more anglicisms from the Wiktionary list. These are combinations of words in German where at least one part is an anglicism.
- **MWE (Multi-word Expression):** A phrase that contains an established anglicism and additional English or German words.
- **ANGNEW:** English words that are not in the Wiktionary list but are identified as anglicisms based on context or usage.
- **NEA (Named Entity Anglicism):** English-language named entities, such as place names or brand names, which are often not part of the language integration process but still contribute to false positives in the detection.

For consistency, the annotation process uses **Prodigy** for manual review and labeling. Some labels (e.g., **MWE**, **ANGNEW**, **NEA**) are not included in the analysis and are labeled with future work in mind.

---

### Results

The evaluation of **AngloFinder** was carried out on a small gold standard test set. Below are the metrics obtained:

- **Precision:** 88.61
- **Recall:** 83.0
- **F1-Score:** 84.27

The results indicated no significant differences in the distribution of anglicisms between human and machine translations across the corpora. However, a more fine-grained qualitative analysis revealed interesting patterns and tendencies in the usage of anglicisms in different translations.

---

### Citation

Here are the main citations for this project:

Shaitarova, A., Göhring, A., & Volk, M. (2023). *Machine vs. Human: Exploring Syntax and Lexicon in German Translations, with a Spotlight on Anglicisms*. Proceedings of the 24th Nordic Conference on Computational Linguistics (NoDaLiDa), 215–227. [Link to paper](https://aclanthology.org/2023.nodalida-1.22)


