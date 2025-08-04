# RNAtox

<img src="graphical_abstract_7.png" alt="drawing" width="200"/>

RNAtox is a code to classify the caspase toxicity and gene knockdown of antisense oligonucleotide (ASO) sequences and generate explanations of k-mers that cause caspase toxicity and gene knockdown using Local Interpretable Model-Agnostic Explanations (LIME), Anchors explanations, and SHapley Additive exPlanations (SHAP).

The RNAtox framework is highly versatile (coded in Google Colab and Jupyter Notebook), with options that can be further developed and optimized by the users: it can accept any user-defined datasets (or datasets available in any repository). It uses pyTorch library for tensor computation with GPU acceleration. The architecture of the classifier is composed of five principal components: (1) a Temporal Convolutional Network (TCN) branch, (2) a projection and attention mechanism applied to RNA-FM embeddings from RNA_FM_T12 foundation model from the RNA-FM library, a 12-layer transformer pre-trained on large RNA corpora, (3) a feature fusion module, (4) a multi-layer LSTM block, and (5) a fully connected classification head. The classifier model was analyzed with different metrics (precision, accuracy, recall, MCC, F1 scores, Matthews correlation coefficient (MCC), and Cohen’s kappa score. Then, the confusion matrix is visualized.

To provide interpretability, three model-agnostic explanation methods were applied: LIME Anchor, and SHAP. The ASO sequences were tokenized into overlapping k-mers (k=3 as chosen by user), simulating word-like units in text classification. Any size of k-mers may be chosen by user. Perturbed k-mer sequences were passed to a wrapped prediction function which internally reverted them to full-length sequences for proper embedding and classification. The three explanations are visualized.

# Installation instructions

RNAtox is 100% compatible with Google Colab or Jupyter Notebook platforms developed in Microsoft Windows using Python version 3.11.

RNAtox has the following dependencies: Lime, Anchor-exp, SHAP, RDkit, Pandas, Matplotlib, seborn, sklearn, and pytorch libraries.

# Documentation

The complete documentation about how to run the RNAtox protocol and several tutorials is being developed. The article will be published on line soon: ???

# Get help

The RNAtox is being actively developed and some issues may arise or you may need extra help to run RNAtox. In those cases, there are two main ways to get help:

1) Open a new issue in this repository
Or 
2) write an email to André Silva Pimentel (a_pimentel@puc-rio.br) (I will do my best to answer your questions as soon as possible).

# License

RNAtox is available under MIT License. See license document for more details. URL and DOI: https://github.com/andresilvapimentel/RNAtox ()

# Contributors

This code was written under collaboration:
Ana Stern da Fonseca Kruel (Undergraduate student), Mariam Sarhan (Undergraduate student), and Andre Silva Pimentel (supervisor).

