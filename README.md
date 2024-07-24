# XAI Taxonomic Guide for Clinical Decision Support Systems


![Project Logo](ai33.png)

## 
This Taxonomic Guide is designed to support CDSS developers in finding suitable XAI methods for their applications. Commonly used XAI models and related clinical use cases are listed below.

This repository was created as part of the PhD project of Dr. Lasantha Ranwaala, University of South Australia.

To follow our taxonomy, user need to answer three basic questions about the CDSS they intended to generate explanations .
1.	What is the input data type of the CDSS?
2.	What is the output type of the CDSS?
3.	Does the CDSS require an explanation model that is inherently easy to understand from the start (White box), or can it be added after the model has undergone training (post-hoc)?

### [Structured Data Inputs](#structured_data)
### [Imaging Data Inputs](#images)



## Structured_Data
## XAI Application for CDSS Models with Structured Data Inputs
| CDSS Output Category | XAI Model Type | Model Specifity  | XAI model/s| Clinical Scenario  |
|----------------------|----------------|---------------|----------|----------------------------|
|           |             | |                                                                            |                                                                                                                          |
| Binnary Calssification    | Post-hoc                  | Model-Agonostic | LIME                                                                       | [Sleep apnea prediction](https://www.sciencedirect.com/science/article/pii/S1877050922012406)<br/>[Breast Cancer Metastasis prediction](https://doi.org/10.1109/TBME.2023.3282840)                                                 |
|                           |                           |                 |                                                                            | [Detection of COVID-19 before the onset of symptoms](https://doi.org/10.1016/j.imu.2022.100941)                                                                |
|                           |                           |                 | Modified LIME                                                              | [COVID-19 prediction](https://doi.org/10.1016/j.ijcce.2023.01.003)                                                                                                 |
|                           |                           |                 | SHAP                                                                       | [Predicting Occurrence of Acute Kidney Injury after Cardiac surgery](https://doi.org/10.31083/j.rcm2408229)                                                  |
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



## Images
## XAI Application for CDSS Models with Medical Imaging Data Inputs

| CDSS Output Category      | XAI Model Type            | Model Specifity | XAI model/s                                                                       | Clinical Scenario                                                                                                  |
|---------------------------|---------------------------|-----------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Binary classification     | Post-hoc                  | Model-specific  | Semantic-Powered Explainable Model-Free Few-Shot Learning Scheme *                | [Diagnose of COVID-19](https://doi.org/10.1109/jbhi.2022.3205167)                                                  |
|                           |                           |                 | Confident-CAM                                                                     | [Improving Heat Map Interpretation in Chest X-Ray Classification](https://doi.org/10.1109/BIBM58861.2023.10386065) |
|                           |                           | Model-agnostic  | LIME                                                                              | [Diabetic Retinopathy Detection](https://doi.org/10.1109/Confluence60223.2024.10463499)                            |
|                           | Built-in Interpretability | Model-specific  | NeuroIGN                                                                          | Image guided brain tumor surgery - 146                                                                             |
|                           |                           |                 | ExPN-Net                                                                          | pulmonary nodule diagnosis - 207                                                                                   |
|                           |                           |                 | MProtoNet                                                                         | Brain Tumur Classification using mpMRI - 227                                                                       |
|                           |                           |                 | CT-xCOV                                                                           | COVID-19 diagnosis using Deep Learning (DL) on CT-scans -173                                                       |
|                           |                           |                 |                                                                                   |                                                                                                                    |
| Multiclass classification | Post-hoc                  | Model-agnostic  | EnsembleXAI                                                                       | Prediction of the<br/>mortality risk of community-acquired pneumonia and COVID-19  - 44                            |
|                           |                           |                 | EGAE                                                                              | Detection of Melanoma  - 7                                                                                         |
|                           |                           |                 | SHaP                                                                              | diagnosis of  Acute Lymphoblastic Leukemia - 164                                                                   |
|                           |                           |                 |                                                                                   | Exploring Brain Tumor Segmentation and Patient Survival: An Interpretable Model Approach - 176                     |
|                           |                           |                 |                                                                                   |  predict the severity level of Alzimer Disease using MRI images - 243                                              |
|                           |                           |                 |                                                                                   | Detecting contrast phase in abdominal CT Scan -236                                                                 |
|                           |                           |                 | MARNet                                                                            | Parkinson's severity diagnosis - 156                                                                               |
|                           |                           |                 |                                                                                   |                                                                                                                    |
|                           |                           |                 | ML-ConvNet                                                                        | Classification of antimicrobial resistance - 56                                                                    |
|                           |                           | Model-specific  | NeuroXAI                                                                          | Prediction of brain tumors -47                                                                                     |
|                           |                           |                 | ResNet-152 combined with Grad–CAM                                                 | Endoscopic image classification - 36                                                                               |
|                           |                           |                 | X-mir                                                                             | Explainable<br/>image retrieval -32                                                                                |
|                           |                           |                 | Grad- CAM                                                                         | diagnosis of  Acute Lymphoblastic Leukemia - 164                                                                   |
|                           |                           |                 |                                                                                   | Exploring Brain Tumor Segmentation and Patient Survival: An Interpretable Model Approach - 176                     |
|                           |                           |                 | MiMICRI                                                                           | cardiovascular image classification - 221                                                                          |
|                           |                           |                 | IEDL-segmentation-of-heart-tissu                                                  | semantic segmentation of histological structures in heart tissue -244                                              |
|                           |                           |                 | IMFSegNet                                                                         | Quantification of intramuscular fat in histological sections - 16                                                  |
|                           | Built-in Interpretability | Model-specific  | RedFormer                                                                         | Detection of Gallballder cancer 10                                                                                 |
|                           |                           |                 | I-AI                                                                              | Diagnosis support for X-Ray - 223                                                                                  |
|                           |                           |                 |  Interpretable Deep Learning Approach for Skin Cancer Categorization              | Skin Cancer Categorisation - 288                                                                                   |
|                           |                           |                 | Hybrid Swin Deformable Attention U-Net for Medical Image Segmentation (SDAH-Unet) | medical image segmentation - 200                                                                                   |
|                           |                           |                 | TR-SE-Net                                                                         | detecting colorectal polyps promptly and accurately - 291                                                          |
|                           |                           |                 |                                                                                   |                                                                                                                    |
| Functional Output         |                           | Model-specific  | scifAI                                                                            | immunological synapse and functional characterization of therapeutic antibodies - 193                              |





