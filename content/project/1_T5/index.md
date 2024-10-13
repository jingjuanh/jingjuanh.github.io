---
title: Distributed Fine-Tuning and Testing of T5 Model for Question Answering System
date: 2024-05-30
external_link: https://github.com/CatherineYellow/spark_project
tags:
  - Fine-Tuning
  - Distributed Computing
  - T5 Model
---

- Preprocessed SQuAD v2 dataset based on the T5 model paper, formatting inputs as question-context pairs and
targets as answer segments.
- Fine-tuned T5 model using Huggingface and Ray frameworks in a distributed setup.
- Deployed the fine-tuned model as a SparkNLP service, integrated Kafka for message streaming, and conducted
performance testing on the T5 model.

<!--more-->
