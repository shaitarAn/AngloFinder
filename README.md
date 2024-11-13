# anglicism_detection

# AngloFinder: Anglicism Detection in German Texts

## Overview

**AngloFinder** is a tool for detecting anglicisms (English loanwords and phrases) in German textual data. It uses two main methods and several look-up resources to identify and analyze anglicisms in a variety of German corpora. This tool is built on a combination of string-matching techniques, natural language processing (NLP), and linguistic resources like Wiktionary and custom datasets.

This repository contains the code and documentation for **AngloFinder**, which includes:

- Methods for detecting anglicisms in German text
- Tools for analyzing lexical and morphological features of translations
- Evaluation results and discussion on the impact of anglicisms in machine translation (MT)

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
