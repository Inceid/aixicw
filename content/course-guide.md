---
title: Course Guide
description: A concise guide to the present and emerging landscape of clinical AI.
tags:
  - intro
---
## Preamble
This session comprises an overview of major updates and applications in clinical and biomedical frontier Artificial Intelligence models across clinical medicine, including an overview and case-based application of ethical, risk, and evaluative frameworks useful for health providers and medical students.

Biomedical AI is changing rapidly with the emergence of large, reusable **foundation models**, **generative AI**, and **agentic systems** that can operate across text, images, audio, electronic health records, and other forms of biomedical data. The goal of this session is to give medical students a practical framework for thinking critically about the opportunities and challenges of this period.

See the [[Learning Objectives]] for this session. See [[Where to go next]] after listening. Slides [here](https://docs.google.com/presentation/d/17L9VC1WhcyDxxsv-2kL6qAX_ZWb9ZhKi3b988b-zba4/edit?usp=sharing).

----
## [[Scope]]
We *will cover*:

- Generative, Agentic, and Foundation models,
- Examples of AI already deployed in clinical medicine,
- Emerging clinical and biomedical applications,
- Ethical/professional issues,
- Equity and health justice,
- Clinical implementation,
- Biomedical research and data analysis,
- A general framework for evaluating AI systems.

We *will not cover*:

- Technical or mathematical foundations of machine learning,
- Detailed model architectures,
- How to use AI for studying,
- Every available AI product or model,
- Existential or catastrophic risks associated with AI,
- Superintelligence.

However, resources for out-of-scope topics will be available at the end of the presentation.

----
## Presenter
Suraj, MS4 at Tufts, interested in psychiatry and public health, on a research year at NIH.

----
## AI is already embedded in clinical practice

- **Autonomous diabetic retinopathy screening**, in which an AI system can analyze retinal images and generate a diagnostic output without specialist interpretation.
- **Computer-aided colonoscopy**, where computer vision systems identify possible polyps in real time.
- **Stroke triage systems**, which can identify suspected large-vessel occlusions and accelerate clinical workflows.
- **Ambient AI scribes**, which transcribe clinical encounters and generate draft documentation.
- **AI-assisted clinical information retrieval**, including newer systems that synthesize medical literature and clinical reference material.

---

## How We Got Here

| Era          | Dominant Paradigm                     | Basic Idea                                                                                           |
| ------------ | ------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| 1960s onward | **Rule-based systems**                | Humans explicitly encode rules and logical relationships.                                            |
| 1990s onward | **Classical machine learning**        | Models learn statistical patterns from data.                                                         |
| 2010s onward | **Deep learning**                     | Neural networks learn increasingly complex features directly from raw data.                          |
| 2020s onward | **Foundation models / Generative AI** | Models are pretrained on very large datasets and adapted across many downstream tasks.               |
| 2025–today   | **Agents / multi-agent systems**      | Models increasingly plan, use tools, and execute multistep goals with less direct human supervision. |

Avanzo et al. provide a broader history of this progression in medical imaging.[1]

---

## [[Glossary|Terminology]]

**AI:** a program that can perform tasks that ordinarily require human intelligence.

**Machine Learning:** techniques used to train an AI system to learn patterns from data rather than relying entirely on pre-programmed rules.

**Supervised Learning:** training using data paired with known outcomes or labels against which model predictions can be compared.
- *E.g.* training an image classifier using chest radiographs labeled as "pneumonia" or "no pneumonia."

**Self-Supervised Learning:** training using structure already present in otherwise unlabeled data rather than relying on human-provided labels.
- Large language models provide an intuitive example. Given:

> Her presentation is most consistent with acute decompensated heart ___

- the model learns to predict the next token—in this case, something like **failure**.
- Repeated across enormous amounts of text, this process allows models to learn statistical representations of language and concepts.

**Foundation Model:** a model trained on broad data at large scale that can subsequently be adapted to many different downstream tasks.
- Rather than training a separate model from scratch for every task, a foundation model provides a reusable base that is also flexibly applicable across *many kinds of problem settings and data types*.
- Currently, foundation models exist that can operate on text, images, audio, video, electronic health records, molecular or genomic data, or combinations of these modalities.

**Generative AI:** AI that generates new data from input data.
- Outputs can include text, images, audio, video, molecular structures, structured clinical information.
- Large language models such as GPT-family models are one subtype of generative AI.

**Agentic AI:** AI that can plan and execute goals with relatively limited human supervision.
- *The more autonomy/scope a system has to act, the more important become questions of oversight, permissions, failure recovery, and accountability.*

---

## How to Think About AI
Use the [[scorecard|clinical AI scorecard]] as a consistent rubric for evaluating any system.

### 1. What problem is the model trying to solve?
- Is the task:
	- classification?
	- prediction?
	- detection?
	- decision support?
	- workflow automation?
- Where does that task sit in the clinical workflow?

### 2. What data is being used?
- Examples:
	- clinical text,
	- imaging,
	- pathology,
	- laboratory data,
	- claims data,
- Whom does the data represent? (Do all populations have equitable access to MRI in their area?)

### 3. What is the output or prediction target?
- Examples:
	- a diagnosis,
	- a risk score,
	- predicted healthcare utilization,
	- an image annotation,
	- generated text,
	- a clinical recommendation,
	- an action.
- The target should correspond to the clinical problem we actually care about. Where this is not the case, the rationale for using a proxy should be disclosed.
- A model can predict its chosen target accurately while still solving the wrong problem.

### 4. What are the predictor variables?
- What information can the model actually see?
- What is missing?
	- clinical context,
	- social determinants of health,
	- care received outside the health system,
	- populations underrepresented in the training data,
	- outcomes that are difficult to measure.

### 5. How is performance measured?
- Possible metrics include:
	- sensitivity,
	- specificity,
	- positive predictive value,
	- discrimination,
	- clinical outcomes,
	- workflow efficiency,
- "Accuracy" is *not enough*.

### 6. What are the benefits, risks, and harms?
See the frameworks discussed later. Examples:
- bias and inequity,
- privacy,
- deskilling,
- accountability,
- environmental and socioeconomic effects.

This scorecard can be applied to almost any AI system without requiring detailed knowledge of its architecture.

---

## Example: How to Think About GPTs
- **Problem:** next-token prediction.
- **Data:** large corpora of text and, increasingly, other modalities.
- **Output:** a probability distribution over possible next tokens.
- **Predictors:** the preceding input tokens and representations learned during training.
- **Training objective:** reduce the discrepancy between predicted and observed tokens across training examples.
- **Downstream behavior:** repeated next-token prediction can produce paragraphs, explanations, code, summaries, dialogue, and other complex outputs.

---

## AI in Medicine Today
### Autonomous diagnosis

Abràmoff et al. evaluated an autonomous AI system for diabetic retinopathy screening in primary care.[3]

### Computer-aided detection

Repici et al. evaluated real-time computer-aided detection during colonoscopy and found increased adenoma detection with AI assistance.[4]

### Workflow acceleration

Martinez-Gutierrez et al. studied automated large-vessel occlusion detection during acute stroke workflows. Implementation reduced time to thrombectomy initiation by approximately 11 minutes.[5]

### Ambient documentation
Tierney et al. described more than 2.5 million uses of ambient AI scribes within The Permanente Medical Group during approximately one year of deployment.[6]

### AI Systems Tomorrow?
The next generation of systems may operate across a much broader portion of the clinical and biomedical workflow.

---

## Responsible Use

A technically successful model does not automatically produce a clinically useful intervention.

Wiens et al. describe responsible medical AI development as a process extending from selection of the clinical problem through data selection, evaluation, ethical analysis, prospective deployment, monitoring, and eventual clinical integration.[8]

Useful questions include:

- Is the problem clinically important?
- Are the training data appropriate?
- Who participated in defining the problem?
- What constitutes "ground truth"?
- What failure modes exist?
- Has the system been evaluated prospectively?
- Does performance persist after deployment?
- How are failures detected?
- Who is accountable when the system is wrong?

---

## Risks
A useful high-level risk taxonomy, adapted from the MIT AI Risk Repository:

| Risk Domain                       | Examples                                                                  |
| --------------------------------- | ------------------------------------------------------------------------- |
| **Discrimination & Toxicity**     | unequal performance, discriminatory allocation, toxic outputs             |
| **Privacy & Security**            | exposure of sensitive information, data leakage, insecure systems         |
| **Misinformation**                | false or misleading outputs, fabricated evidence                          |
| **Malicious Use**                 | fraud, manipulation, cyberattacks                                         |
| **Loss of Agency**                | overreliance, automation bias, deskilling                                 |
| **Socioeconomic / Environmental** | unequal access, labor effects, resource and energy use                    |
| **System Safety & Failure**       | unreliable behavior, failure under distribution shift, unintended actions |

These risks can also be mapped onto familiar biomedical ethics principles. (*Exercise*)

---

## Case: Algorithmic Bias in Population Health

Consider a health system using a commercial algorithm to identify patients for enrollment in a high-risk care management program.

The program includes additional nursing follow-up, primary care access, and expedited specialty referral.

The algorithm uses longitudinal clinical and utilization data to generate a risk score. Patients above a particular threshold are referred or automatically enrolled.

Before deploying such a system, ask:

- Who was represented in the training population?
- What outcome is the model actually predicting?
- Which predictors are included?
- Which variables may encode existing structural inequities?
- How does performance differ across populations?
- What happens at the decision threshold?
- Is there external validation?
- How will the system be monitored after deployment?

Obermeyer et al. studied a widely used commercial population-health algorithm and showed why these questions matter.[9]

The model used **future healthcare spending** as a proxy for **future healthcare need**.

Because healthcare spending differed systematically between Black and White patients with comparable levels of illness, the apparently reasonable target encoded an existing structural disparity. At the same risk score, Black patients were substantially sicker than White patients.

Changing the prediction target substantially reduced the observed racial disparity.[9]

---

## What Would You Do Differently?

### 1. Population / Training Data
- Who is represented?
- Who is missing?
- Are subgroup sample sizes sufficient to evaluate performance?

### 2. Prediction Target
- Is the target a clinically meaningful outcome (number of patient deaths in an ICU ward) or a proxy thereof (bundled cost of ICU resource utilization relative to hospital-wide utilization)?

### 3. Predictor Variables
- Which variables should be included?
- Could some variables reproduce inequities already present in the healthcare system?
- Would removing a variable reduce bias, or hide the pathway through which bias operates?

### 4. Validation, Monitoring, and Accountability

- Has the model been externally validated?
- Does performance change across sites, populations, time, workflows?
- Who monitors the system after deployment?
- Who intervenes when it fails?

### 5. Decision Rule

What happens after the model produces a score? Are scores stratified, thresholded in any way before a decision is made? When does a human see the numbers?

---

## What Should I Know as a Medical Student?

Identify via the scorecard:
- **Problem:** classification? prediction? generation? decision support?
- **Data:** text? imaging? claims? EHR? genomics?
- **Output:** diagnosis? score? text? image? action?
- **Predictors:** what information enters the model?
- **Performance:** how is success measured?
- **Benefits, risks, and harms:** what happens when the system enters clinical practice?

Then, evaluate:
- Is the output clinically meaningful?
- Is the evidence appropriate for the way the tool is being used?
- How does the model perform across relevant patient subgroups?
- Is the reasoning or evidence sufficiently interpretable for the task?
- What are the privacy and information-security protections?
- Is the model robust outside its original training environment?
- What happens when it is wrong?
- Who is responsible for detecting and correcting failure?
- What human skill should remain even if the task becomes automated?

---

## Resources
Resources are organized by the four learning-objective domains used in the presentation.

### Ethics & Professionalism

- Algorithmic Justice League
- American Medical Association
- Coalition for Health AI
- MIT AI Risk Repository

### Equity & Population Health

- NIH AIM-AHEAD Consortium
- Algorithmic Justice League
- Data for Black Lives
- MIT Critical Data

### Clinical Implementation

- Coalition for Health AI
- FDA resources on AI-enabled medical devices
- Health-system implementation and evaluation literature

### Research & Biomedical Data Analysis

- NIH AI resources
- Biomedical informatics curricula
- Open-source model and data-science resources

----

## Disclosure
Presentation content and accompanying course text were written by Suraj Joshi. Generative AI was used for literature review and editorial assistance. All modified text was reviewed and verified by the author. Figures are attributed individually where applicable.

## References (for Slides)

1. Avanzo M, Stancanello J, Pirrone G, Drigo A. **The Evolution of Artificial Intelligence in Medical Imaging: From Computer Science to Machine and Deep Learning.** *Cancers (Basel).* 2024;16(21):3702. doi:10.3390/cancers16213702.

2. Moor M, Banerjee O, Shakeri Hossein Abad Z, et al. **Foundation models for generalist medical artificial intelligence.** *Nature.* 2023;616:259–265. doi:10.1038/s41586-023-05881-4.

3. Abràmoff MD, Lavin PT, Birch M, Shah N, Folk JC. **Pivotal trial of an autonomous AI-based diagnostic system for detection of diabetic retinopathy in primary care offices.** *npj Digital Medicine.* 2018;1:39. doi:10.1038/s41746-018-0040-6.

4. Repici A, Badalamenti M, Maselli R, et al. **Efficacy of Real-Time Computer-Aided Detection of Colorectal Neoplasia in a Randomized Trial.** *Gastroenterology.* 2020;159(2):512–520.e7. doi:10.1053/j.gastro.2020.04.062.

5. Martinez-Gutierrez JC, Kim Y, Salazar-Marioni S, et al. **Automated Large Vessel Occlusion Detection Software and Thrombectomy Treatment Times: A Cluster Randomized Clinical Trial.** *JAMA Neurology.* 2023;80(11):1182–1190. doi:10.1001/jamaneurol.2023.3206.

6. Tierney AA, Gayre G, Hoberman B, et al. **Ambient Artificial Intelligence Scribes: Learnings after 1 Year and over 2.5 Million Uses.** *NEJM Catalyst Innovations in Care Delivery.* 2025;6(5). doi:10.1056/CAT.25.0040.

7. Shanmugam D, Agrawal M, Movva R, Chen IY, Ghassemi M, Jacobs M, Pierson E. **Generative Artificial Intelligence in Medicine.** *Annual Review of Biomedical Data Science.* 2025;8:199–226. doi:10.1146/annurev-biodatasci-103123-095332.

8. Wiens J, Saria S, Sendak M, et al. **Do no harm: a roadmap for responsible machine learning for health care.** *Nature Medicine.* 2019;25:1337–1340. doi:10.1038/s41591-019-0548-6.

9. Obermeyer Z, Powers B, Vogeli C, Mullainathan S. **Dissecting racial bias in an algorithm used to manage the health of populations.** *Science.* 2019;366(6464):447–453. doi:10.1126/science.aax2342.

See [[references|References and source links]] for additional material.
