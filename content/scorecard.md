---
title: Clinical AI Scorecard
description: Six questions for identifying and evaluating any clinical AI system.
---

You do not need to memorize every model architecture. Ask the same six questions consistently.

## 1. What problem is the model trying to solve?

Is the task classification, prediction, generation, detection, ranking, decision support, workflow automation, or autonomous action? Where does it sit in the clinical workflow?

## 2. What data are being used?

Text, imaging, pathology, laboratory data, genomics, claims, electronic health records, audio, wearables, or patient-reported data? Where did the data come from, and whom do they represent?

## 3. What is the output or prediction target?

A diagnosis, risk score, predicted utilization, annotation, generated text, recommendation, or action? The target should correspond to the clinical problem we actually care about. A model can predict its chosen target accurately while still solving the wrong problem.

## 4. What are the inputs or predictor variables?

What information can the model see? What is missing—clinical context, social determinants of health, care outside the health system, underrepresented populations, or difficult-to-measure outcomes?

## 5. How is performance measured?

Consider sensitivity, specificity, positive predictive value, calibration, discrimination, clinical outcomes, workflow effects, and subgroup performance. **Accuracy alone is rarely enough.**

## 6. What are the benefits, risks, and harms?

What happens when the system enters clinical practice? Consider clinical benefit, patient safety, bias and inequity, privacy, security, misinformation, interpretability, automation bias, deskilling, workflow effects, accountability, and environmental or socioeconomic effects.

| Risk domain | Examples |
| --- | --- |
| **Discrimination and toxicity** | Unequal performance, discriminatory allocation, toxic outputs |
| **Privacy and security** | Exposure of sensitive information, data leakage, insecure systems |
| **Misinformation** | False or misleading outputs, fabricated evidence |
| **Malicious use** | Fraud, manipulation, cyberattacks |
| **Loss of agency** | Overreliance, automation bias, deskilling |
| **Socioeconomic and environmental** | Unequal access, labor effects, resource and energy use |
| **System safety and failure** | Unreliable behavior, distribution shift, unintended actions |

> [!tip] Medical ethics provides a second lens
> For narrower clinical questions, also consider **beneficence, nonmaleficence, autonomy, and justice**.

## A compact version

| Dimension | Ask |
| --- | --- |
| **Problem** | What task is the model performing? |
| **Data** | What information was used, and whom does it represent? |
| **Output** | What does the system produce or predict? |
| **Predictors** | What can the model see, and what is missing? |
| **Performance** | How is success measured, including across subgroups? |
| **Consequences** | What benefits, risks, and harms follow in practice? |

See the [[course-guide#Case Algorithmic Bias in Population Health|population-health case]] for an applied example.
