# Classifying Spanish se constructions: from bag of words to language models

This repository contains the corpus created for the paper "Classifying Spanish se constructions: from bag of words to language models" published at the SEPLN journal 2020 april edition. A notebook to reproduce the paper experiments is also included.

## Corpus

The corpus is available as three files:

* [se_classification_train.csv](./se_classification_train.csv): training split.
* [se_classification_test.csv](./se_classification_test.csv): test split.
* [se_classification_balanced_train.csv](./se_classification_balanced_train.csv): oversampled version of training split (for reproducing the paper experiments).

They are tab-separated files with header and one row per text. The columns are:

* **id**: unique identifier of the text.
* **text**
* **se_tag**: "se" usage, among `se-mark`, `expl`, `obj`, `iobj`.

## Notebook

The experiments can be reproduced by using the provided [multiclass_classification_SE.ipynb](./multiclass_classification_SE.ipynb) notebook. We recommend to use a [Google Colab](colab.research.google.com/) instance with GPU.

## Citations

If you use this corpus or the notebook in this repository, please cite us as

    AVAILABLE SOON! (once the journal version is released)
