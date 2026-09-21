---
title: Glossary
description: Plain-language definitions for the central concepts in the session.
---

## Artificial intelligence

**AI:** a program that can perform tasks that ordinarily require human intelligence.

AI is the broadest category in this glossary.

## Machine learning

**Machine learning:** techniques used to train an AI system to learn patterns from data rather than relying entirely on pre-programmed rules.

## Supervised learning

**Supervised learning:** training using data paired with known outcomes or labels against which model predictions can be compared.

For example, an image classifier might be trained using chest radiographs labeled “pneumonia” or “no pneumonia.”

## Self-supervised learning

**Self-supervised learning:** training using structure already present in otherwise unlabeled data rather than relying on human-provided labels.

Large language models provide an intuitive example. Given:

> Her presentation is most consistent with acute decompensated heart ___

the model learns to predict the next token—in this case, something like **failure**. Repeated across enormous amounts of text, this process allows models to learn statistical representations of language and concepts.

## Foundation model

**Foundation model:** a model trained on broad data at large scale that can subsequently be adapted to many downstream tasks.

Instead of training a separate model from scratch for every task, a foundation model provides a reusable base. Foundation models may operate on text, images, audio, video, electronic health records, molecular or genomic data, or combinations of these modalities.

## Generative AI

**Generative AI:** AI that generates new data from input data.

Outputs may include text, images, audio, video, code, molecular structures, or structured clinical information. Large language models are one subtype of generative AI.

## Agentic AI

**Agentic AI:** AI that can plan and execute goals with relatively limited human supervision.

An agent may interpret a goal, determine intermediate steps, retrieve information, use tools, evaluate intermediate results, and revise its plan. As autonomy and scope increase, oversight, permissions, failure recovery, and accountability become more important.

## Related concepts

- **Predictor or input:** information available to the model when generating an output.
- **Target or outcome:** the quantity the model is trained or evaluated to predict.
- **Proxy:** a measurable quantity used in place of the outcome actually of interest.
- **Validation:** evaluation of model performance using data not used to fit the model.
- **Dataset shift:** a change in the data distribution between development and real-world use.

Next: [[scorecard|apply the clinical AI scorecard]].
