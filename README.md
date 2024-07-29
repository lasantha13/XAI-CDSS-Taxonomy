# XAI Taxonomic Guide for Clinical Decision Support Systems


![Project Logo](ai33.png)

## 
This Taxonomic Guide is designed to support CDSS developers in finding suitable XAI methods for their applications. Commonly used XAI models and related clinical use cases are listed below.

This repository was created as part of the PhD project of Dr. Lasantha Ranwaala, University of South Australia.

To follow our taxonomy, user need to answer three basic questions about the CDSS they intended to generate explanations .
```
1.	What is the input data type of the CDSS?
2.	What is the output type of the CDSS?
3.	Does the CDSS require an explanation model that is inherently easy to understand from the start (White box), or can it be added after the model has undergone training (post-hoc)?
```


### Table of Contents
1. [Clinical Use Cases: CDSS with Structured Data Inputs](#structured_data)
2. [Clinicla Use Cases : CDSS with Imaging Data Inputs](#images)
3. [Clinicla Use Cases : CDSS with Other Data Type Inputs](#images)
4. [XAI Models : Structured Data Inputs](#xai_1)
5. [XAI Models : Medical Imaging Inputs](#xai_2)
6. [XAI Models : Other Data type Inputs](#xai_3)




## Structured_Data
## Clinical Uses : XAI Application for CDSS Models with Structured Data Inputs
| CDSS Output Category | XAI Model Type | Model Specifity  | XAI Model| Clinical Scenario  |
|----------------------|----------------|---------------|----------|----------------------------|
|           |             | |                                                                            |                                                                                                                          |
| Binnary Calssification    | Post-hoc                  | Model-Agonostic | LIME                                                                       | [Sleep apnea prediction](https://www.sciencedirect.com/science/article/pii/S1877050922012406) ,<br/>[Breast Cancer Metastasis prediction](https://doi.org/10.1109/TBME.2023.3282840)                                                 |
|                           |                           |                 |                                                                            | [Detection of COVID-19 before the onset of symptoms](https://doi.org/10.1016/j.imu.2022.100941)                                                                |
|                           |                           |                 | Modified LIME                                                              | [COVID-19 prediction](https://doi.org/10.1016/j.ijcce.2023.01.003)                                                                                                 |
|                           |                           |                 | SHAP                                                                       | [Predicting Occurrence of Acute Kidney Injury after Cardiac surgery](https://doi.org/10.31083/j.rcm2408229)                                                  |
|                           |                           |                 |                                                                            | [Cervical cancer prediction using behavioral risk factors](https://doi.org/10.1016/j.health.2024.100324)                                                           |
|                           |                           |                 |                                                                            | [Predicting the conversion of clinically isolated syndrome (CIS) to clinically definite multiple scleÂ­rosis (CDMS)](https://doi.org/10.1016/j.msard.2024.105614) |
|                           |                           |                 |                                                                            |  [predict 1-year survival after palliative radiotherapy (RT) for bone<br/>metastasis](https://doi.org/10.1200/CCI.24.00027)                                |
|                           |                           |                 |                                                                            | [Breast cancer detection](https://doi.org/10.1109/I2CT61223.2024.10543965)                                                                                            |
|                           |                           |                 | SHAP & LIME                                                                | [Prediction of diabetes Management](https://go.openathens.net/redirector/unisa.edu.au?url=https://www.proquest.com/scholarly-journals/explainable-artificial-intelligence-xai/docview/2858093357/se-2?accountid=14649),<br/>[Diabetes prediction using machine learning](https://doi.org/10.1049/htl2.12039) ,<br/>[C-Section prediction](https://doi.org/10.1016/j.compbiomed.2022.105671)                                                            |
|                           |                           |                 |                                                                            | [Parkinsonâ€™s Speech  Detection](https://doi.org/10.1109/ICCAR61844.2024.10569414)                                                                                    |
|                           |                           |                 | SHAP,LIME,ELI5,Qlattice                                                    | [Detection of Polycystic Ovary Syndrome](https://doi.org/10.3390/asi6020032)                                                                              |
|                           |                           |                 | SHAP,Decision tree ,Rule based system                                      | [Intensive care unit mortality prediction of neonate patients](https://doi.org/10.1016/j.jbi.2022.104216)                                                        |
|                           |                           |                 | SHAP,LIME,ELI5,Qlattice, Anchors                                           | [Gestational diabetes mellitus prediction using clinical and laboratory markers](https://doi.org/10.1080/23311916.2024.2330266)                                 |
|                           |                           |                 | DeepExplainer                                                              | [Lung Cancer Detection](https://doi.org/10.1016/j.cmpb.2023.107879)                                                                                               |
|                           |                           |                 | MVR-GA                                                                     | [Accurate hepatotoxicity prediction](https://doi.org/10.1109/BIBM55620.2022.9995667)                                                                                  |
|                           |                           |                 | Araucana XAI                                                               | [Prediction of hospitalization outcome of patients with liver dieases. & Prediction of death in ICU patients](https://doi.org/10.1016/j.artmed.2022.102471)        |
|                           | Built-in Interpretability | Model-specific  | OVBLR-SFE                                                                  | [An intensive care unit readmission prediction case for liver transplantation patients](https://doi.org/10.1016/j.eswa.2023.121138)                                |
|                           |                           |                 |                                                                            |                                                                                                                          |
| Multiclass Classification | Post-hoc                  | Model-Agonostic | ELIS5                                                                      | [Brain tumor classification](https://doi.org/10.1016/j.procs.2023.01.182)                                                                                           |
|                           |                           |                 | SHaP                                                                       | [Predict the risk factors related to the direct association between obesity and comorbidities](https://doi.org/10.1109/e-Science58273.2023.10254948)                        |
|                           |                           |                 | LIME                                                                       | [Predict cardiovascular disease risk](https://doi.org/10.1109/BIBM58861.2023.10385315)                                                                                |
|                           |                           |                 | AnEMIC                                                                     | [A Framework for benchmarking ICD Coding Models](https://doi.org/10.18653%2Fv1%2F2022.emnlp-demos.11)                                                                      |
|                           |                           |                 | SHAP & LIME                                                                | [Predicting fetal abnormalities base on  cardiotocography readings](https://doi.org/10.1109/AAIAC60008.2023.10465473)                                                   |
|                           |                           | Model-specific  | VDJMiner                                                                   | [Mine the underlying medical conditions and predict the prognosis of COVID-19](https://doi.org/10.1093/bib/bbac555)                                         |
|                           |                           |                 |                                                                            |                                                                                                                          |
|                           | Built-in Interpretability | Model-specific  | Explainable Argumentation with Assumptions, Preferences, and Goals (ABA+G) | [Managing co-morbidity and clinical guidelines](https://doi.org/10.1002/lrh2.10391)                                                                      |
| Functional Output         | Post-hoc                  | Model-Agonostic | Explainable Fold                                                           | [AlphaFold Prediction with Explainable AI](https://doi.org/10.1145/3580305.3599337)                                                                            |
|                           |                           |                 |                                                                            |                                                                                                                          |
|                           |                           | Model-specific  | SurvSHAP(t)                                                                | [Time-dependent explanations of machine learning survival models](https://doi.org/10.1016/j.knosys.2022.110234)                                                     |
|                           |                           |                 | SurvSHAP(t), SurvLIME, Ceteris Paribus Survival Profile                    | [Survival in Bone Marrow Transplantation Trials](https://doi.org/10.3390/biomedinformatics3030048)                                                                     |



## Images
## Clinical Uses : XAI Application for CDSS Models with Medical Imaging Data Inputs

| CDSS Output Category      | XAI Model Type            | Model Specifity | XAI Mmodel                                                                       | Clinical Scenario                                                                                                  |
|---------------------------|---------------------------|-----------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Binary classification     | Post-hoc                  | Model-specific  | Semantic-Powered Explainable Model-Free Few-Shot Learning Scheme *                | [Diagnose of COVID-19](https://doi.org/10.1109/jbhi.2022.3205167)                                                  |
|                           |                           |                 | Confident-CAM                                                                     | [Improving Heat Map Interpretation in Chest X-Ray Classification](https://doi.org/10.1109/BIBM58861.2023.10386065) |
|                           |                           | Model-agnostic  | LIME                                                                              | [Diabetic Retinopathy Detection](https://doi.org/10.1109/Confluence60223.2024.10463499)                            |
|                           | Built-in Interpretability | Model-specific  | NeuroIGN                                                                          | [Image guided brain tumor surgery](https://link.springer.com/article/10.1007/s10916-024-02037-3)                                                                             |
|                           |                           |                 | ExPN-Net                                                                          | [pulmonary nodule diagnosis](https://doi.org/10.1016/j.bspc.2023.105646)                                                                                   |
|                           |                           |                 | MProtoNet                                                                         | [Brain Tumur Classification using mpMRI](https://proceedings.mlr.press/v227/wei24a.html)                                                                       |
|                           |                           |                 | CT-xCOV                                                                           | [COVID-19 diagnosis using Deep Learning (DL) on CT-scans](https://doi.org/10.1109/WINCOM59760.2023.10322985)                                                       |
|                           |                           |                 |                                                                                   |                                                                                                                    |
| Multiclass classification | Post-hoc                  | Model-agnostic  | EnsembleXAI                                                                       | [Prediction of the<br/>mortality risk of community-acquired pneumonia and COVID-19](https://doi.org/10.1109/TAI.2022.3153754)                            |
|                           |                           |                 | EGAE                                                                              | [Detection of Melanoma](https://doi.org/10.1016/j.compbiomed.2023.106613)                                                                                         |
|                           |                           |                 | SHaP                                                                              | [diagnosis of  Acute Lymphoblastic Leukemia](https://doi.org/10.1016/j.eij.2024.100479)                                                                   |
|                           |                           |                 |                                                                                   | [Exploring Brain Tumor Segmentation and Patient Survival: An Interpretable Model Approach](https://ceur-ws.org/Vol-3684/p01.pdf)                     |
|                           |                           |                 |                                                                                   |  [predict the severity level of Alzimer Disease using MRI images](https://doi.org/10.1109/CAISAIS59399.2023.10270042)                                              |
|                           |                           |                 |                                                                                   | [Detecting contrast phase in abdominal CT Scan](https://link.springer.com/article/10.1007/s00330-024-10769-6)                                                                 |
|                           |                           |                 | MARNet                                                                            | [Parkinson's severity diagnosis](https://doi.org/10.1016/j.compbiomed.2024.107959)                                                                               |
|                           |                           |                 |                                                                                   |                                                                                                                    |
|                           |                           |                 | ML-ConvNet                                                                        | [Classification of antimicrobial resistance](https://doi.org/10.1109/ACCESS.2022.3216896)                                                                    |
|                           |                           | Model-specific  | NeuroXAI                                                                          | [Prediction of brain tumors](https://link.springer.com/article/10.1007/s11548-022-02619-x)                                                                                     |
|                           |                           |                 | ResNet-152 combined with Grad–CAM                                                 | [Endoscopic image classification](https://doi.org/10.3390/s23063176)                                                                               |
|                           |                           |                 | X-mir                                                                             | [Explainable<br/>image retrieval](https://openaccess.thecvf.com/content/WACV2022/html/Hu_X-MIR_EXplainable_Medical_Image_Retrieval_WACV_2022_paper.html)                                                                                |
|                           |                           |                 | Grad- CAM                                                                         | [diagnosis of  Acute Lymphoblastic Leukemia](https://doi.org/10.1016/j.eij.2024.100479)                                                                   |
|                           |                           |                 |                                                                                   | [Exploring Brain Tumor Segmentation and Patient Survival: An Interpretable Model Approach](https://ceur-ws.org/Vol-3684/p01.pdf)                     |
|                           |                           |                 | MiMICRI                                                                           | [cardiovascular image classification](https://dl.acm.org/doi/abs/10.1145/3630106.3659011)                                                                          |
|                           |                           |                 | IEDL-segmentation-of-heart-tissu                                                  | [semantic segmentation of histological structures in heart tissue](https://doi.org/10.1016/j.compbiomed.2024.108624)                                              |
|                           |                           |                 | IMFSegNet                                                                         | [Quantification of intramuscular fat in histological sections](https://doi.org/10.1016/j.csbj.2023.07.031)                                                  |
|                           | Built-in Interpretability | Model-specific  | RedFormer                                                                         | [Detection of Gallballder cancer](https://doi.org/10.1016/j.media.2022.102676)                                                                                 |
|                           |                           |                 | I-AI                                                                              | [Diagnosis support for X-Ray](https://openaccess.thecvf.com/content/WACV2024/html/Pham_I-AI_A_Controllable__Interpretable_AI_System_for_Decoding_Radiologists_WACV_2024_paper.html)                                                                                  |
|                           |                           |                 |  Interpretable Deep Learning Approach for Skin Cancer Categorization              | [Skin Cancer Categorisation](https://doi.org/10.1109/ICCIT60459.2023.10508527)                                                                                   |
|                           |                           |                 | Hybrid Swin Deformable Attention U-Net for Medical Image Segmentation (SDAH-Unet) | [medical image segmentation](https://doi.org/10.1109/SIPAIM56729.2023.10373513)                                                                                   |
|                           |                           |                 | TR-SE-Net                                                                         | [detecting colorectal polyps promptly and accurately](https://doi.org/10.1109/ACCESS.2024.3402818)                                                          |
|                           |                           |                 |                                                                                   |                                                                                                                    |
| Functional Output         |                           | Model-specific  | scifAI                                                                            | [Immunological synapse and functional characterization of therapeutic antibodies](https://www.nature.com/articles/s41467-023-43429-2)                              |



## XAI_1
### XAI Models Details - CDSS with Structred Data Inputs
<table>
    <tr>
        <td>Model </td>
        <td colspan="3"> Model Output (Binarry/ Muliclass Classfication/ Funtional)</td>
        <td colspan="2">Timing of interpretability  </td>
        <td colspan="2">Model Specificity </td>
        <td>Explainable Methods  </td>
    </tr>
    <tr>
        <td></td>
        <td>Bi</td>
        <td>Multi</td>
        <td>Func</td>
        <td>Built-in</td>
        <td>Post-hoc</td>
        <td>Agonostic</td>
        <td>specific</td>
        <td> </td>
    </tr>
    <tr>
        <td>ABA+G</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>combination of Transition-based Medical Recommendation (TMR) Model and Explainable Argumentation with Assumptions, Preferences, and Goals  </td>
    </tr>
    <tr>
        <td>Anchors</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Rule-based Explanation </td>
    </tr>
    <tr>
        <td>AnEMIC</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Rule-based Systems </td>
    </tr>
    <tr>
        <td><a href="https://github.com/bmi-labmedinfo/araucana-xai">Araucana XAI</a></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Rule-based Systems </td>
    </tr>
    <tr>
        <td>Ceteris Paribus Survival Profile</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>Feature Importance, Survival Analysis </td>
    </tr>
    <tr>
        <td>Decision tree </td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Rule-based Systems </td>
    </tr>
    <tr>
        <td><a href="https://
github.com/niyazwani/DeepXplainer.git">Deep Explainer</a></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td>feature importance and visualization techniques </td>
    </tr>
    <tr>
        <td>ELIS5</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Explanation by Linear Interactions </td>
    </tr>
    <tr>
        <td><a href="https://eli5.readthedocs.io/en/latest/overview.html">Explainable Fold</a></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Rule-based Systems </td>
    </tr>
    <tr>
        <td><a href="https://github.com/marcotcr/lime?tab=readme-ov-file">LIME</a></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Feature Importance, Feature Attribution </td>
    </tr>
    <tr>
        <td>Modified LIME</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Feature Importance, Feature Attribution </td>
    </tr>
    <tr>
        <td>MVR-GA</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Rule Extraction </td>
    </tr>
    <tr>
        <td>OVBLR-SFE</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Salient Feature Estimation, Bayesian Logistic Regression </td>
    </tr>
    <tr>
        <td>Qlattice</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Rule-based Systems </td>
    </tr>
    <tr>
        <td>SHAP</td>
        <td>+</td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Feature Importance, Feature Attribution </td>
    </tr>
    <tr>
        <td>SurvLIME</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>Feature Importance, Survival Analysis </td>
    </tr>
    <tr>
        <td>SurvSHAP(t)</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>Feature Importance, Survival Analysis </td>
    </tr>
</table>


