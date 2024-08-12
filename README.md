# XAI Taxonomic Guide for Clinical Decision Support Systems


![Project Logo](ai33.png)

## 
This Taxonomic Guide is designed to support CDSS developers in finding suitable XAI methods for their applications. Commonly used XAI models and related clinical use cases are listed below.

This repository was created as part of the PhD project of Dr. Lasantha Ranwaala, University of South Australia.

To follow our taxonomy, user need to answer three basic questions about the CDSS they intended to generate explanations .
```
1.	What is the input data type of the CDSS?
2.	What is the output type of the CDSS?
3.	Does the CDSS require an inherently understandable model to generate explanations, or can explanations be added after the model is built?
```


### Table of Contents
#### A. Classification of XAI Models/Methods in CDSS Based on Input Data Types with Clinical Application Examples
1. [XAI Models/Methods in CDSS with Structured Data Inputs](#structured_data)
2. [XAI Models/Methods in CDSS with Imaging Data Inputs](#images)
3. [XAI Models/Methods in CDSS with Other* Data Inputs](#images)

*Molecular Structures (Chemical compounds, drug molecules), Protein Structures, Signals and Omics Data 

#### B. XAI Method/Models Features
4. [XAI Models : Structured Data Inputs](#xai_1)
5. [XAI Models : Medical Imaging Inputs](#xai_2)
6. [XAI Models : Other Data type Inputs](#xai_3)




## Structured_Data
## XAI Models/Methods in CDSS with Structured Data Inputs
| CDSS Output Category | XAI Model Type | Model Specificity  | XAI Model| Clinical Scenario  |
|----------------------|----------------|---------------|----------|----------------------------|
|           |             | |                                                                            |                                                                                                                          |
| Binary Classification   | Post-hoc                  | Model-Agnostic | LIME                                                                       | [Sleep apnoea prediction](https://www.sciencedirect.com/science/article/pii/S1877050922012406) ,<br/>[Breast Cancer Metastasis prediction](https://doi.org/10.1109/TBME.2023.3282840)                                                 |
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
|                           |                           |                 |                                                     | [Gestational diabetes mellitus prediction using clinical and laboratory markers](https://doi.org/10.1080/23311916.20242330266)                                                                              |
|                           |                           |                 |                                                     | [Osteoporosis risk prediction](https://doi.org/10.1016/j.heliyon.2023.e22456)                                                                              |
|                           |                           |                 | DeepExplainer                                                              | [Lung Cancer Detection](https://doi.org/10.1016/j.cmpb.2023.107879)                                                                                               |
|                           |                           |                 | MVR-GA                                                                     | [Accurate hepatotoxicity prediction](https://doi.org/10.1109/BIBM55620.2022.9995667)                                                                                  |
|                           |                           |                 | Araucana XAI                                                               | [Prediction of hospitalization outcome of patients with liver dieases. & Prediction of death in ICU patients](https://doi.org/10.1016/j.artmed.2022.102471)        |
|                           | Built-in Interpretability | Model-specific  | OVBLR-SFE                                                                  | [An intensive care unit readmission prediction case for liver transplantation patients](https://doi.org/10.1016/j.eswa.2023.121138)                                |
|                           |                           |                 | Decision Tree,Rule based system                                      | [Intensive care unit mortality prediction of neonate patients](https://doi.org/10.1016/j.jbi.2022.104216)                                                        |
|                           |  |  | GSInquire                                                                  | kidney injury of COVID-19 patients -198                                |
|                           | |   | Tropical Geometry-Based Interpretable ML Method                                                                  | Identifying heart failure patients that are eligible for advanced therapies -274                                |
|                           |                           |                 |                                                                            |                                                                                                                          |
| Multiclass Classification | Post-hoc                  | Model-Agonostic | ELIS5                                                                      | [Brain tumor classification](https://doi.org/10.1016/j.procs.2023.01.182)                                                                                           |
|                           |                           |                 | SHaP                                                                       | [Predict the risk factors related to the direct association between obesity and comorbidities](https://doi.org/10.1109/e-Science58273.2023.10254948)                        |
|                           |                           |                 | LIME                                                                       | [Predict cardiovascular disease risk](https://doi.org/10.1109/BIBM58861.2023.10385315)                                                                                |
|                           |                           |                 | AnEMIC                                                                     | [A Framework for benchmarking ICD Coding Models](https://doi.org/10.18653%2Fv1%2F2022.emnlp-demos.11)                                                                      |
|                           |                           |                 | SHAP & LIME                                                                | [Predicting fetal abnormalities base on  cardiotocography readings](https://doi.org/10.1109/AAIAC60008.2023.10465473)     |
|                           | Built-in Interpretability | Model-specific  | Explainable Argumentation with Assumptions, Preferences, and Goals (ABA+G) | [Managing co-morbidity and clinical guidelines](https://doi.org/10.1002/lrh2.10391)                                                                      |
|      |                |  |                                                            |                                                                            |
|  Functional Output                          |   Post-hoc                        | Model-Agonostic  | SurvSHAP(t)                                                                | [Time-dependent explanations of machine learning survival models](https://doi.org/10.1016/j.knosys.2022.110234)                                                     |
|                           |                           |                 | SurvSHAP(t), SurvLIME, Ceteris Paribus Survival Profile                    | [Survival in Bone Marrow Transplantation Trials](https://doi.org/10.3390/biomedinformatics3030048)                                                                     |



## Images
## XAI Models/Methods in CDSS with Imaging Data Inputs

| CDSS Output Category      | XAI Model Type            | Model Specifity | XAI Model/Method                                                                      | Clinical Scenario                                                                                                  |
|---------------------------|---------------------------|-----------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| Binary classification     | Post-hoc                  | Model-specific  | Semantic-Powered Explainable Model-Free Few-Shot Learning Scheme               | [Diagnose of COVID-19](https://doi.org/10.1109/jbhi.2022.3205167)                                                  |
|                           |                           |                 | Confident-CAM                                                                     | [Improving Heat Map Interpretation in Chest X-Ray Classification](https://doi.org/10.1109/BIBM58861.2023.10386065) |
|                           |                           | Model-agnostic  | LIME                                                                              | [Diabetic Retinopathy Detection](https://doi.org/10.1109/Confluence60223.2024.10463499)                            |
|                           | Built-in Interpretability | Model-specific  | NeuroIGN                                                                          | [Image guided brain tumor surgery](https://link.springer.com/article/10.1007/s10916-024-02037-3)                                                                             |
|                           |                           |                 | ExPN-Net                                                                          | [pulmonary nodule diagnosis](https://doi.org/10.1016/j.bspc.2023.105646)                                                                                   |
|                           |                           |                 | MProtoNet                                                                         | [Brain Tumur Classification using mpMRI](https://proceedings.mlr.press/v227/wei24a.html)                                                                       |
|                           |                           |                 | CT-xCOV                                                                           | [COVID-19 diagnosis using Deep Learning (DL) on CT-scans](https://doi.org/10.1109/WINCOM59760.2023.10322985)                                                       |
|                           |                           |                 |                                                                                   |                                                                                                                    |
| Multiclass classification | Post-hoc                  | Model-agnostic  | EnsembleXAI                                                                       | [Prediction of the<br/>mortality risk of community-acquired pneumonia and COVID-19](https://doi.org/10.1109/TAI.2022.3153754)                            |
|                           |                           |                 | EGAE                                                                              | [Detection of Melanoma](https://doi.org/10.1016/j.compbiomed.2023.106613)                                                                                         |
|                           |                           |                 | SHaP                                                                              | [Diagnosis of  Acute Lymphoblastic Leukemia](https://doi.org/10.1016/j.eij.2024.100479)                                                                   |
|                           |                           |                 |                                                                                   | [Exploring Brain Tumor Segmentation and Patient Survival: An Interpretable Model Approach](https://ceur-ws.org/Vol-3684/p01.pdf)                     |
|                           |                           |                 |                                                                                   |  [predict the severity level of Alzimer Disease using MRI images](https://doi.org/10.1109/CAISAIS59399.2023.10270042)                                              |
|                           |                           |                 |                                                                                   | [Detecting contrast phase in abdominal CT Scan](https://link.springer.com/article/10.1007/s00330-024-10769-6)                                                                 |
|                           |                           |                 | MARNet                                                                            | [Parkinson's severity diagnosis](https://doi.org/10.1016/j.compbiomed.2024.107959)                                                                               |
|                           |                           |                 |                                                                                   |                                                                                                                    |
|                           |                           | Model-specific  | NeuroXAI                                                                          | [Prediction of brain tumors](https://link.springer.com/article/10.1007/s11548-022-02619-x)                                                                                     |
|                           |                           |                 | ResNet-152 combined with Grad–CAM                                                 | [Endoscopic image classification](https://doi.org/10.3390/s23063176)                                                                               |
|                           |                           |                 | X-mir                                                                             | [Explainable<br/>image retrieval](https://openaccess.thecvf.com/content/WACV2022/html/Hu_X-MIR_EXplainable_Medical_Image_Retrieval_WACV_2022_paper.html)                                                                                |
|                           |                           |                 | Grad- CAM                                                                         | [Diagnosis of  Acute Lymphoblastic Leukemia](https://doi.org/10.1016/j.eij.2024.100479)                                                                   |
|                           |                           |                 |                                                                                   | [Exploring Brain Tumor Segmentation and Patient Survival: An Interpretable Model Approach](https://ceur-ws.org/Vol-3684/p01.pdf)                     |
|                           |                           |                 | MiMICRI                                                                           | [cardiovascular image classification](https://dl.acm.org/doi/abs/10.1145/3630106.3659011)                                                                          |
|                           |                           |                 | IEDL-segmentation-of-heart-tissu                                                  | [semantic segmentation of histological structures in heart tissue](https://doi.org/10.1016/j.compbiomed.2024.108624)                                              |
|                           |                           |                 | IMFSegNet                                                                         | [Quantification of intramuscular fat in histological sections](https://doi.org/10.1016/j.csbj.2023.07.031)                                                  |
|                           | Built-in Interpretability | Model-specific  | RedFormer                                                                         | [Detection of Gallballder cancer](https://doi.org/10.1016/j.media.2022.102676)                                                                                 |
|                           |                           |                 | I-AI                                                                              | [Diagnosis support for X-Ray](https://openaccess.thecvf.com/content/WACV2024/html/Pham_I-AI_A_Controllable__Interpretable_AI_System_for_Decoding_Radiologists_WACV_2024_paper.html)                                                                                  |
|                           |                           |                 |  Interpretable Deep Learning Approach for Skin Cancer Categorization              | [Skin Cancer Categorisation](https://doi.org/10.1109/ICCIT60459.2023.10508527)                                                                                   |
|                           |                           |                 | Hybrid Swin Deformable Attention U-Net for Medical Image Segmentation (SDAH-Unet) | [medical image segmentation](https://doi.org/10.1109/SIPAIM56729.2023.10373513)                                                                                   |
|                           |                           |                 | MICA                                                                         | Skin Lesion Diagnosis -158                                                          |
|                           |                           |                 |                                                                                   |                                                                                                                    |
| Functional Output         |        Post-hoc                   | Model-agnostic  | Eigen Visualization                                                                           | Automated Detection of Colorectal Polyp  - 291                              |
|          |        Hybrid(Built-in Interpretability + Post Hoc)                   | Model-specific + Model Agnosti  | scifAI                                                                            | [Immunological synapse and functional characterization of therapeutic antibodies](https://www.nature.com/articles/s41467-023-43429-2)                              |

## Other Data types
## XAI Models/Methods in CDSS with Other* Data Inputs

| CDSS Input Data type                                                           |  CDSS Output Category          | Model Type                | Model Specifity |         XAI Model/s                  |      Clinical Scenario                                                                                        |
|---------------------------------------------------------------------------|---------------------------|---------------------------|-----------------|---------------------------|----------------------------------------------------------------------------------------------|
| Molecular Structures (Chemical compounds, drug molecules)                 | Binnary Calssification    | Built-in Interpretability | Model-specific  | AttentiveSkin             | [Prediction of risk of skin irritation](https://pubs.acs.org/doi/full/10.1021/acs.chemrestox.3c00332)                                                  |
| Protein Structures                                                        | Functional                | Post-hoc                  | Model-Agonostic | Explainable Fold          | [AlphaFold Prediction with Explainable AI](https://doi.org/10.1145/3580305.3599337)                                                |
| Signals (ECG, EEG, EMG)                                                   | Multiclass Classification | Post-hoc                  | Model-Agonostic | SHaP                      | [predict cardiovascular status using  ECG](https://doi.org/10.1109/DTPI59677.2023.10365417)                                               |
|                                                                           | Binnary Calssification    | Post-hoc                  | Model-Agonostic | SHaP                      | [predictors in post-stroke recovery from EEG](https://doi.org/10.1016/j.neucom.2024.127622)                                            |
|                                                                           |                           | Post-hoc                  | Model-specific  |  GlepNet                  | [Epilepsy detection using EEG](https://doi.org/10.1109/TAI.2024.3406289)                                                           |
| Omics Data (Genomics, Gene expression matrix and single-cell sequencing)) | Binary classification     | Post-hoc                  | Model-specific  |  GNNExplainer             | [Covid19 severity assessment using bronchoalveolar lavage fluid](https://doi.org/10.1109/BIBM58861.2023.10385934) |
|                                                                           |                           |                           |                 | MV-BRS                    | [Hepatotoxicity prediction](https://doi.org/10.1109/BIBM58861.2023.10385784)                                                              |
|                                                                           | Multiclass Classification | Post-hoc                  | Model-specific  | VDJMiner                  | [Mine the underlying medical conditions and predict the prognosis of COVID-19](https://doi.org/10.1093/bib/bbac555)             |
|                                                                           |                           |                           |                 | Gradiant based approached | [Predicting Antimicrobial Resistance (AMR) from genomic sequence data](https://doi.org/10.1109/ACCESS.2022.3216896)                    |

*Molecular Structures (Chemical compounds, drug molecules), Protein Structures, Signals and Omics Data 

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
        <td>Combination of Transition-based Medical Recommendation (TMR) Model and Explainable Argumentation with Assumptions, Preferences, and Goals  </td>
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
        <td><a href="https://github.com/dalgu90/icd-coding-benchmark">AnEMIC</a></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Integrated Gradients and attention scores </td>
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
        <td>Uses a decision tree structure for interpretability. </td>
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
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>feature importance and visualization techniques </td>
    </tr>
    <tr>
        <td><a href="https://eli5.readthedocs.io/en/latest/overview.html">ELIS5</a></td>
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
        <td><a href="https://github.com/MLDMXM2017/MVR-GA">MVR-GA</a></td>
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
        <td><a href="https://github.com/xqw42/OVBLR-SFE">OVBLR-SFE</a></td>
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
        <td><a href="https://docs.abzu.ai/docs/guides/getting_started/quick_start.html">Qlattice</a></td>
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
        <td><a href="https://shap.readthedocs.io/en/latest/tabular_examples.html">SHAP</a></td>
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
        <td><a href="https://github.com/imatge-upc/SurvLIMEpy">SurvLIME</a></td>
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
        <td><a href="https://github.com/MI2DataLab/survshap">SurvSHAP(t)</a></td>
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


## XAI_2
### XAI Models Details - CDSS with Image Data Inputs

<table>
    <tr>
        <td>Model </td>
        <td colspan="3">Output Type</td>
        <td colspan="2">Timing of interpretability</td>
        <td colspan="2">XAI Model speciity</td>
        <td>Explainable Methods  </td>
    </tr>
    <tr>
        <td></td>
        <td>Bi</td>
        <td>Multi</td>
        <td>Func</td>
        <td>Built-in Interpretability</td>
        <td>Post-hoc</td>
        <td>Model-Agonostic</td>
        <td>Model-specific</td>
        <td>Explainable Methods  </td>
    </tr>
    <tr>
        <td><a href="https://github.com/JoanaNRocha/Confident-CAM">Confident-CAM</a> </td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>Heatmaps, Feature Importance </td>
    </tr>
    <tr>
        <td><a href="https://github.com/ismailelbouknify/CT-xCOV">CT-xCOV</a></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Textual justification; Visualisation </td>
    </tr>
    <tr>
        <td><a href="https://github.com/KhaosResearch/EGAE">EGAE</a></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Image Segmentation </td>
    </tr>
    <tr>
        <td>Eigen Visualisation</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>localization</td>
    </tr>
    </td>
    </tr>
    <tr>
        <td>EnsembleXAI</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>image Classfication </td>
    </tr>
    <tr>
        <td><a href=" https://github.com/isha-67/CervicalCancerStudy">Explainable Contrastive and Cost-Sensitive Learning for Cervical Cancer</a></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>Contrastive Learning, Cost-Sensitive Learning, Visualization </td>
    </tr>
    <tr>
        <td><a href="https://github.com/KumoLiu/explainablePN">ExPN-Net</a></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Visualization, Feature Importance, Heatmaps </td>
    </tr>
    <tr>
        <td><a href="https://github.com/wlc2424762917/SDAH UNet">SDAH-Unet</a></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Attention Maps, Feature Visual </td>
    </tr>
    <tr>
        <td><a href="https://github.com/UARK-AICV/IAI">I-AI</a></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Attention Maps, Heatmaps, Feature Importance </td>
    </tr>
    <tr>
        <td><a href="https://github.com/applied-systems-biology/sheepfat">IMFSegNet</a></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Image Segmentation </td>
    </tr>
    <tr>
        <td><a href="https://github.com/Faysal-MD/An-Interpretable-Deep-Learning-
Approach-for-Skin-Cancer-Categorization-IEEE2023
">Interpretable DL for Skin Cancer Categorization</a></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Feature Importance, Heatmaps, Visualization </td>
    </tr>
    <tr>
        <td><a href="https://github.com/mathali/IEDL-segmentation-of-heart-tissue">Intrinsically explainable DL for heart tissue segmentation</a></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Semantic Segmentation, Visualization </td>
    </tr>
    <tr>
        <td>LIME</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Feature Importance , Heatmaps </td>
    </tr>
    <tr>
        <td>MARNet </td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>visualization and feature importance  </td>
    </tr>
    <tr>
        <td>MICA</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Concept Alignment, Feature Attribution </td>
    </tr>
    <tr>
        <td>MiMICRI</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>Counterfactual Explanations, Feature Importance </td>
    </tr>
    <tr>
        <td>ML-ConvNet</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>Image Segmentation </td>
    </tr>
    <tr>
        <td>MProtoNet</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Case-Based Reasoning, Feature Importance </td>
    </tr>
    <tr>
        <td>NeuroGen</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Visualization, Feature Importance </td>
    </tr>
    <tr>
        <td>NeuroXAI</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>image Classfication, Image Segmentation </td>
    </tr>
    <tr>
        <td>RadFormer</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>Image Localization </td>
    </tr>
    <tr>
        <td>ResNet-152 combined with Grad–CAM</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>image Classfication </td>
    </tr>
    <tr>
        <td>scifAI </td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td>+</td>
        <td>+</td>
        <td>+</td>
        <td>&quot;</td>
    </tr>
    <tr>
        <td>Semantic-Powered Explainable Model-Free Few-Shot Learning Scheme</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>image Classfication </td>
    </tr>
    <tr>
        <td>X-mir</td>
        <td></td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>image Classfication </td>
    </tr>
</table>

## XAI_3
### XAI Models Details - CDSS with Other* Data Inputs

<table>
    <tr>
        <td>Model </td>
        <td>Input Data type</td>
        <td colspan="3">Output Type</td>
        <td colspan="2">Timing of interpretability</td>
        <td colspan="2">XAI Model speciity</td>
        <td>Explainable Methods  </td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td>Bi</td>
        <td>Multi</td>
        <td>Fun </td>
        <td>Built-in Interpretability</td>
        <td>Post-hoc</td>
        <td>Model-Agonostic</td>
        <td>Model-specific</td>
        <td>Explainable Methods  </td>
    </tr>
    <tr>
        <td>AM-EEGNet:</td>
        <td>EEG Signal</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td></td>
        <td>SHaP (Feature Importance) </td>
    </tr>
    <tr>
        <td>AttentiveSkin</td>
        <td>Moleecular Structure</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td>+</td>
        <td>+</td>
        <td>+</td>
        <td>+</td>
        <td>SHAP (Feature Importance), Attention Mechanisms, Visualization </td>
    </tr>
    <tr>
        <td>GlepNet</td>
        <td>EEG Signal</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>Grad-CAM identifies the most important features and regions that contribute to the model’s predictions </td>
    </tr>
    <tr>
        <td>GNNExplainer</td>
        <td>Gene Expression Matrix </td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td> identifies the most important features and subgraphs that contribute to the model’s predictions </td>
    </tr>
    <tr>
        <td>Multi-View Learning-Based Bayesian Ruleset Extraction algorithm (MV-BRS)</td>
        <td>Omics</td>
        <td>+</td>
        <td></td>
        <td></td>
        <td></td>
        <td>+</td>
        <td></td>
        <td>+</td>
        <td>Bayesian rule extraction </td>
    </tr>
 
   
  
</table>
*Molecular Structures (Chemical compounds, drug molecules), Protein Structures, Signals and Omics Data 
