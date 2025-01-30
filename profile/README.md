# Welcome to the VIEWS Platform!

![GitHub branch check runs](https://img.shields.io/github/check-runs/views-platform/views-pipeline-core/main)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/views-platform/views-pipeline-core)
![GitHub Release](https://img.shields.io/github/v/release/views-platform/views-pipeline-core)

<div style="width: 100%; max-width: 1500px; height: 400px; overflow: hidden; position: relative;">
  <img src="https://pbs.twimg.com/profile_banners/1237000633896652800/1717069203/1500x500" alt="VIEWS Twitter Header" style="position: absolute; top: -50px; width: 100%; height: auto;">
</div>

The [**Violence & Impacts Early Warning System (VIEWS)**](https://viewsforecasting.org/) is an award-winning conflict prediction system that generates monthly forecasts for violent conflicts across the world up to three years in advance, at both country and sub-country levels of analysis. The views-platform contains several repositories, individual packages and documentation that encapsulates the entire process of developing, experimenting, training, evaluating, and deploying the VIEWS machine learning model pipeline.

Use our [interactive data dashboard](https://data.viewsforecasting.org/) to explore our latest predictions of future armed conflict.

---

## Table of contents

<!-- toc -->

- [Rationale](#rationale-a-robust-machine-learning-pipeline-for-early-warning-systems)
- [Key Processes](#key-processes-of-the-views-pipeline) 
- [Key Features](#key-features-of-the-views-pipeline)
- [Pipeline Overview](#pipeline-overview)
- [Platform Structure and Contents](#views-platform-organization-structure-and-contents)
- [Further Resources and Documentation](#further-resources-and-documentation)
- [About the VIEWS Project](#about-the-views-project)

<!-- tocstop -->

---

## Rationale: a Robust Machine Learning Pipeline for Early Warning Systems 

Conflict forecasting plays a vital role in early warning systems (EWS), where timely and accurate predictions can inform critical decisions in high-stakes scenarios. However, existing pipelines often fall short in operational reliability, scalability, and transparency, limiting their effectiveness for real-world applications. To address these challenges, a new benchmark in machine learning operations (MLOps) is proposed, focusing on the development of a robust, reliable, and ethical pipeline tailored for EWS.
Our initiative emphasizes combining cutting-edge MLOps practices with conflict forecasting requirements, ensuring the pipeline is not only **technically sound** but also **adaptable** to dynamic conditions and aligned with **ethical standards**. The primary goal is to create a **transparent** and **scalable** infrastructure that supports accurate predictions, rapid model updates, and seamless operations, thereby bridging the gap between research prototypes and fully operational systems. Additionally, we rely on **Open Source** and **FAIR** (Findable, Accessible, Interoperable, and Reusable) principles to guide the design, promoting transparency, accessibility, and collaboration.

---

## Key Processes of the VIEWS Pipeline

Achieving the goals stated in our rationale for building a robust ML pipeline involves several core iterative processes: 

- **Developing:** Creating and refining machine learning models.
- **Experimentation:** Testing and validating various model configurations and approaches.
- **Training:** Training models with relevant data.
- **Evaluating:** Assessing model performance and accuracy.
- **Deploying:** Implementing models in a production environment to generate monthly true-future forecasts. 

---

## Key Features of the VIEWS Pipeline

Developing and maintaining the VIEWS relies on multiple key features:

- **Centralized Logging Framework:** At the heart of the pipeline is a comprehensive logging framework designed to enhance visibility, traceability, and system transparency. 
- **Monitoring and Input Drift Detection:** To maintain the accuracy and reliability of predictions, the pipeline features robust monitoring mechanisms for both model monitoring, as well as monitoring input data in order to ensure timely intervention in cases of deviations.
- **Branching and Synchronization Strategy:** A branching model separates stable production code from ongoing development, minimizing the risk of disruptions during updates. Synchronization workflows will ensure that updates to tightly coupled ML and non-ML components occur in unison, preventing dependency issues.
- **Versioning and Artifact Management:** As versioning is crucial for ensuring reproducibility and facilitating troubleshooting, the pipeline includes robust version control for all artifacts, including models, datasets, and configurations.
- **Modular and Scalable Infrastructure:** The modular design of the pipeline supports scalability and adaptability in dynamic conditions, in turn allowing for simplified maintenance and upgrades.

---

## Pipeline Overview

The overall structure, as well as the core processes in the VIEWS machine learning pipeline are vizualized below:

![VIEWS pipeline diagram](https://raw.githubusercontent.com/views-platform/views-pipeline-core/main/documentation/pipeline_diagram001.png)

---

## VIEWS-Platform Organization: Structure and Contents 

The views-platform hosts all of the necesary components for producing forecasts utilizing the VIEWS ML pipeline. The modularity of the pipeline allows for components to be maintained in individual repositories. The execution of the pipeline relies on the following repositories: 

- [views-pipeline-core:](https://github.com/views-platform/views-pipeline-core) Contains the main components necesary for the execution of the VIEWS pipeline, handling data ingestion, preprocessing, model and ensemble training, evaluation, and experiment tracking.
- [views-models:](https://github.com/views-platform/views-models) Contains all of the implemented VIEWS models, at both PRIO-GRID-month and country-month levels of analysis, along with information about prediction targets, input data and model algorithms. 
- [views-stepshifter:](https://github.com/views-platform/views-stepshifter) Contains the VIEWS Stepshifter model class for time-series forecasts.
- [views-hydranet:](https://github.com/views-platform/views-hydranet) Contains the VIEWS HydraNet model class for spatiotemporal forecasts.
- [views-evaluation:](https://github.com/views-platform/views-evaluation) Contains the tools for storing, calculating and managing evaluation metrics for time-series forecasting models.
- [docs:](https://github.com/views-platform/views-evaluation) Contains high-level documentation of the views-platform, the pipeline and its components, along with detailed instructions, guides and information about the project and how to interact with the individual components. 

For more in-depth information about each repository and its contents, please see the detailed repository-specific README files:
- Pipeline execution: [views-pipeline-core](https://github.com/views-platform/views-pipeline-core/blob/main/README.md)
- About the VIEWS models: [views-models](https://github.com/views-platform/views-models/blob/main/README.md)
- About VIEWS stepshifter: [views-stephifter](https://github.com/views-platform/views-stepshifter/blob/main/README.md)
- About VIEWS HydraNet: [views-hydranet](https://github.com/views-platform/views-hydranet/blob/main/README.md)
- Forecast evaluation: [views-evaluation](https://github.com/views-platform/views-evaluation/blob/main/README.md)

---

## Further Resources and Documentation

The previous iteration of the VIEWS model, [Fatalities002](https://viewsforecasting.org/early-warning-system/models/fatalities002/), generated forecasts for state-based armed conflict during each month in a rolling 3-year window. 

The following links cover **modelling documentation** for Fatalities002:
- [Prediction models and input variables in main ensemble](https://viewsforecasting.org/views_documentation_models_fatalities002/)
- [Levels of analysis and dependent variables](https://viewsforecasting.org/wp-content/uploads/VIEWS_documentation_LevelsandOutcomes.pdf)
- [Partitioning and time shifting data for training, calibration, testing/forecasting, model weighting, and out-of-sample evaluation](https://viewsforecasting.org/wp-content/uploads/VIEWS_Documentation_Partitioningandtimeshifting_Fatalities002.pdf)
- [Ensembling and calibration](https://viewsforecasting.org/wp-content/uploads/VIEWS_documentation_Ensembling_Fatalities002.pdf)

For VIEWS-specific **infrastructure documentation**, please refer to following GitHub repositories:
- [`ingester3`: Loading input data into the views database](https://github.com/UppsalaConflictDataProgram/ingester3)
- [`viewser`: Accessing input data from views database](https://github.com/prio-data/viewser)
- [`views_api`: Our API for accessing predictions](https://github.com/prio-data/views_api)

---

## About the VIEWS Project

The VIEWS project is a collaborative effort supported by leading research institutions focused on peace and conflict studies. For more information about the project, visit the [VIEWS Forecasting webpage](https://viewsforecasting.org/).

### Affiliations

- **Peace Research Institute Oslo (PRIO):**
  The [Peace Research Institute Oslo (PRIO)](https://www.prio.org/) conducts research on the conditions for peaceful relations between states, groups, and people. PRIO is dedicated to understanding the processes that lead to violence and those that create sustainable peace. About half of the VIEWS core team is currently located at PRIO.

- **Department of Peace and Conflict Research at Uppsala University:**
  The [Department of Peace and Conflict Research at Uppsala University](https://www.uu.se/en/department/peace-and-conflict-research) is a leading academic institution in the study of conflict resolution, peacebuilding, and security. The department is renowned for its research and education programs aimed at fostering a deeper understanding of conflict dynamics and peace processes. This department also hosts the [Uppsala Conflict Data Program (UCDP)](https://ucdp.uu.se/), a central data source for the VIEWS project. About half of the VIEWS core team is currently located at Uppsala University .


### Funding and Partners

The research presented on this website is the outcome of projects that has received funding from the European Research Council (ERC) under the European Union’s Horizon 2020 research and innovation programme (Grant agreement No. 694640, ViEWS) and Horizon Europe (Grant agreement No. 101055176, ANTICIPATE; and 101069312, ViEWS (ERC-2022-POC1)), Riksbankens Jubileumsfond (Grant agreement No. M21-0002, Societies at Risk), Uppsala University, Peace Research Institute Oslo, the United Nations Economic and Social Commission for Western Asia (ViEWS-ESCWA), the United Kingdom Foreign, Commonwealth & Development Office (GSRA – Forecasting Fatalities in Armed Conflict), the Swedish Research Council (DEMSCORE), the Swedish Foundation for Strategic Environmental Research (MISTRA Geopolitics), the Norwegian MFA (Conflict Trends QZA-18/0227), the United Nations High Commissioner for Refugees (the Sahel Predictive Analytics project  and Global Mapping of Forecasting Systems), the Norwegian Research Council (U FFAC), and the Complex Risk Analytics Fund (CRAF’d, VIEWS-PIN ).


<div style="width: 100%; max-width: 1500px; height: 400px; overflow: hidden; position: relative; margin-top: 50px;">
  <img src="image.png" alt="Funder logos" style="position: absolute; top: -50px; width: 100%; height: auto;">
</div>



