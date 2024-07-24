# XAI Taxonomic Guide for Clinical Decision Support Systems


![Project Logo](ai33.png)


## 
This Taxonomic Guide is designed to support CDSS developers in finding suitable XAI methods for their applications. Commonly used XAI models and related clinical use cases are listed below.
This repository was created as part of the PhD project of Dr. Lasantha Ranwaala, University of South Australia


To follow our taxonomy user, need to answer three basic questions about the CDSS they intended to generate explanations .
1.	What is the input data type of the CDSS?
2.	What is the output type of the CDSS?
3.	Does the CDSS require an explanation model that is inherently easy to understand from the start (White box), or can it be added after the model has undergone training (post-hoc)?


| CDSS Output Category | XAI Model Type | Model Specifity  | XAI model/s| Clinical Scenario  |
|----------------------|----------------|---------------|----------|----------------------------|
|           |             | |                                                                            |                                                                                                                          |
| Binnary Calssification    | Post-hoc                  | Model-Agonostic | LIME                                                                       | Sleep apnea prediction - 20 <br/>Breast Cancer Metastasis prediction- 39                                                 |
|                           |                           |                 |                                                                            | Detection of COVID-19 before the onset of symptoms  - 238                                                                |
|                           |                           |                 | Modified LIME                                                              | COVID-19 prediction - 28                                                                                                 |
|                           |                           |                 | SHAP                                                                       | Predicting Occurrence of Acute Kidney Injury after Cardiac surgery - 21                                                  |
|                           |                           |                 |                                                                            | Cervical cancer prediction using behavioral risk factors - 147                                                           |
|                           |                           |                 |                                                                            | Predicting the conversion of clinically isolated syndrome (CIS) to clinically definite multiple scleÂ­rosis (CDMS) - 174 |
|                           |                           |                 |                                                                            |  predict 1-year survival after palliative radiotherapy (RT) for bone<br/>metastasis - 201                                |
|                           |                           |                 |                                                                            | Breast cancer detection - 220                                                                                            |
|                           |                           |                 | SHAP & LIME                                                                | prediction of diabetes - 34 ,37<br/>C-Section prediction-15                                                              |
|                           |                           |                 |                                                                            | Parkinsonâ€™s Speech  Detection - 255                                                                                    |
|                           |                           |                 | SHAP,LIME,ELI5,Qlattice                                                    | Detection of Polycystic Ovary Syndrome - 59                                                                              |
|                           |                           |                 | SHAP,Decision tree ,Rule based system                                      | Intensive care unit mortality prediction of neonate patients - 13                                                        |
|                           |                           |                 | SHAP,LIME,ELI5,Qlattice, Anchors                                           | Gestational diabetes mellitus prediction using<br/>clinical and laboratory markers - 159                                 |
|                           |                           |                 | DeepExplainer                                                              | Lung Cancer Detection -148                                                                                               |
|                           |                           |                 | MVR-GA                                                                     | Accurate hepatotoxicity prediction - 68                                                                                  |
|                           |                           |                 | Araucana XAI                                                               | Prediction of hospitalization outcome of patients with liver dieases. & Prediction of death in ICU patients. - 14        |
|                           | Built-in Interpretability | Model-specific  | OVBLR-SFE                                                                  | An intensive care unit readmission prediction case for liver transplantation patients -51                                |
|                           |                           |                 |                                                                            |                                                                                                                          |
| Multiclass Classification | Post-hoc                  | Model-Agonostic | ELIS5                                                                      | Brain tumor classification - 5                                                                                           |
|                           |                           |                 | SHaP                                                                       | Predict the risk factors related to the direct association between obesity and comorbidities -254                        |
|                           |                           |                 | LIME                                                                       | Predict cardiovascular disease risk - 253                                                                                |
|                           |                           |                 | AnEMIC                                                                     | A Framework for benchmarking ICD Coding Models - 41                                                                      |
|                           |                           |                 | SHAP & LIME                                                                | Predicting fetal abnormalities base on  cardiotocography readings- 153                                                   |
|                           |                           | Model-specific  | VDJMiner                                                                   | Mine the underlying medical conditions and predict the prognosis of COVID-19 - 3                                         |
|                           |                           |                 |                                                                            |                                                                                                                          |
|                           | Built-in Interpretability | Model-specific  | Explainable Argumentation with Assumptions, Preferences, and Goals (ABA+G) | Managing co-morbidity and clinical guidelines - 189                                                                      |
| Functional Output         | Post-hoc                  | Model-Agonostic | Explainable Fold                                                           | AlphaFold Prediction with Explainable AI - 12                                                                            |
|                           |                           |                 |                                                                            |                                                                                                                          |
|                           |                           | Model-specific  | SurvSHAP(t)                                                                | Time-dependent explanations of machine learning survival models - 27                                                     |
|                           |                           |                 | SurvSHAP(t), SurvLIME, Ceteris Paribus Survival Profile                    | Survival in Bone Marrow Transplantation Trials - 194                                                                     |


| SurvSHAP | [Survival](https://example.com)n Trials - 194 |
|--------------|-------------------------|
|row | [Cell 1](https://example.com) 