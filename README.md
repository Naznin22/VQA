# Visual Question Answering with BERT
This project is a reimplementation of a strong baseline model for Visual Question Answering (VQA), based on the work of [Cyanogenoid](https://github.com/Cyanogenoid/pytorch-vqa/), who also reimplemented Vahid Kazemi and Ali Elqursh's paper, [Show, Ask, Attend, and Answer: A Strong Baseline for Visual Question Answering](https://arxiv.org/abs/1704.03162).

## Overview
The main goal of our work was to explore the performance of BERT in the context of VQA. BERT utilizes Transformers, an attention mechanism that learns contextual relationships between words (or sub-words) in a text.

The figure below illustrates the overall structure of our model:

<br>

![image](https://github.com/user-attachments/assets/6c03c1f1-cea9-46e4-a9b9-6f3d81e85f5c)

In the original model, the question 𝑞 is tokenized into a set of n tokens using a simple embedding layer. These tokens are then fed into an LSTM layer, and the final state of the LSTM is used to represent the question. In our implementation, we use pre-trained BERT to extract sentence embeddings for each question.

We utilized the "base" and "uncased" versions of BERT. The "base" version is smaller than the "large" version, making it more suitable for our limited resources. The "uncased" version ignores casing, which is not significant for our task.

We compared our performance on VQA-real with the baselines proposed in the original paper:

![image](https://github.com/user-attachments/assets/501386aa-5677-44d9-8be5-2e3801005d96)

Figure 8.1: Graph of training (red) and validation (blue) accuracy for VQA-Abstract

<br>
<br>

![image](https://github.com/user-attachments/assets/8d4fb427-5a63-455b-b13e-a4e3d2fd5622)

Figure 8.3: Graph of training (red) and validation (blue) accuracy for VQA-Real

## Results
Our results on VQA-Abstract achieved an accuracy of 61.3%, while VQA-Real reached 57.35%. We compared our baseline model to various other baselines and full VQA models. BERT sentence embeddings are indeed beneficial in the context of VQA, and further research utilizing BERT as the question embedding layer should be pursued. Further implementation and result details can be found in this [file](https://github.com/Naznin22/VQA/blob/main/Final%20Report_edited.pdf).

