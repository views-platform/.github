# Welcome to the VIEWS Platform

![GitHub License](https://img.shields.io/github/license/views-platform/views-pipeline-core)
![GitHub branch check runs](https://img.shields.io/github/check-runs/views-platform/views-pipeline-core/main)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/views-platform/views-pipeline-core)
![GitHub Release](https://img.shields.io/github/v/release/views-platform/views-pipeline-core)

<div style="width: 100%; max-width: 1500px; height: 400px; overflow: hidden; position: relative;">
  <img src="https://pbs.twimg.com/profile_banners/1237000633896652800/1717069203/1500x500" alt="VIEWS Twitter Header" style="position: absolute; top: -50px; width: 100%; height: auto;">
</div>

The [**Violence & Impacts Early Warning System (VIEWS)**](https://viewsforecasting.org/) is an award-winning conflict prediction system that generates monthly forecasts for violent conflicts across the world up to three years in advance, at both country and sub-country levels of analysis. The views-platform contains several repositories, individual packages and documentation that encapsulates the entire process of developing, experimenting, training, evaluating, and deploying the VIEWS machine learning model pipeline.

Use our [interactive data dashboard](https://data.viewsforecasting.org/) to explore our latest predictions of future armed conflict.

> [!CAUTION]
> Please note that this pipeline is **actively under construction**. We're in the **process of development**, meaning it's **not yet ready for operational use**. We're working hard to bring you a robust and fully-functional tool, so stay tuned for updates!

## Table of contents

<!-- toc -->
- [Platform Structure and Contents](#platform-structure-and-contents)
- [Further Resources and Documentation](#further-resources-and-documentation)
- [About the VIEWS Project](#about-the-views-project)

<!-- tocstop -->

## Rationale: a Robust Machine Learning Pipeline for Early Warning Systems 

Conflict forecasting plays a vital role in early warning systems (EWS), where timely and accurate predictions can inform critical decisions in high-stakes scenarios. However, existing pipelines often fall short in operational reliability, scalability, and transparency, limiting their effectiveness for real-world applications. To address these challenges, a new benchmark in machine learning operations (MLOps) is proposed, focusing on the development of a robust, reliable, and ethical pipeline tailored for EWS.
This initiative emphasizes combining cutting-edge MLOps practices with conflict forecasting requirements, ensuring the pipeline is not only technically sound but also adaptable to dynamic conditions and aligned with ethical standards. The primary goal is to create a transparent and scalable infrastructure that supports accurate predictions, rapid model updates, and seamless operations, thereby bridging the gap between research prototypes and fully operational systems.

## Key Features 

## Platform Structure and Contents

### Pipeline Overview

The VIEWS machine learning pipeline involves several key processes:

- **Developing:** Creating and refining machine learning models.
- **Experimentation:** Testing and validating various model configurations and approaches.
- **Training:** Training models with relevant data.
- **Evaluating:** Assessing model performance and accuracy.
- **Deploying:** Implementing models in a production environment to generate monthly true-future forecasts. 

The overall structure of our pipeline and its individual components are visualized below: 

![VIEWS pipeline diagram](https://raw.githubusercontent.com/views-platform/views-pipeline-core/main/documentation/pipeline_diagram001.png)


### Organization Contents

The views-platform includes several repositories necessary for the execution of the pipeline:

- [views-pipeline-core:](https://github.com/views-platform/views-pipeline-core) Contains the main components necesary for the execution of the VIEWS pipeline, handling data ingestion, preprocessing, model and ensemble training, evaluation, and experiment tracking.
- [views-models:](https://github.com/views-platform/views-models) Contains all of the implemented VIEWS models, at both PRIO-GRID-month and country-month levels of analysis, along with information about prediction targets, input data and model algorithms. 
- [views-stepshifter:](https://github.com/views-platform/views-stepshifter) Contains the 
- [views-hydranet:](https://github.com/views-platform/views-hydranet) Contains the 
- [views-evaluation:](https://github.com/views-platform/views-evaluation) Contains the tools for storing, calculating and managing evaluation metrics for time-series forecasting models.
- [docs:](https://github.com/views-platform/views-evaluation) Contains high-level documentation of the views-platform, the pipeline and its components, along with detailed instructions, guides and information about the project and how to interact with the individual components. 

For more in-depth information about each repository and its contents, please see the detailed repository-specific README files.   

## Further Resources and Documentation

**NOTE:** This should be updated once the pipeline is operational!!

The operational fatalities model generates forecasts for state-based armed conflict during each month in a rolling 3-year window. 
The latest iteration, currently in production, is called [Fatalities002](https://viewsforecasting.org/early-warning-system/models/fatalities002/).

The following links cover **modelling documentation** for Fatalities002:
- [Prediction models and input variables in main ensemble](https://viewsforecasting.org/views_documentation_models_fatalities002/)
- [Levels of analysis and dependent variables](https://viewsforecasting.org/wp-content/uploads/VIEWS_documentation_LevelsandOutcomes.pdf)
- [Partitioning and time shifting data for training, calibration, testing/forecasting, model weighting, and out-of-sample evaluation](https://viewsforecasting.org/wp-content/uploads/VIEWS_Documentation_Partitioningandtimeshifting_Fatalities002.pdf)
- [Ensembling and calibration](https://viewsforecasting.org/wp-content/uploads/VIEWS_documentation_Ensembling_Fatalities002.pdf)

For VIEWS-specific **infrastructure documentation**, please refer to following GitHub repositories:
- [`ingester3`: Loading input data into the views database](https://github.com/UppsalaConflictDataProgram/ingester3)
- [`viewser`: Accessing input data from views database](https://github.com/prio-data/viewser)
- [`views_api`: Our API for accessing predictions](https://github.com/prio-data/views_api)



## About the VIEWS Project

The VIEWS project is a collaborative effort supported by leading research institutions focused on peace and conflict studies. For more information about the project, visit the [VIEWS Forecasting webpage](https://viewsforecasting.org/).

### Affiliations

- **Peace Research Institute Oslo (PRIO):**
  The [Peace Research Institute Oslo (PRIO)](https://www.prio.org/) conducts research on the conditions for peaceful relations between states, groups, and people. PRIO is dedicated to understanding the processes that lead to violence and those that create sustainable peace. About half of the VIEWS core team is currently located at PRIO.

- **Department of Peace and Conflict Research at Uppsala University:**
  The [Department of Peace and Conflict Research at Uppsala University](https://www.uu.se/en/department/peace-and-conflict-research) is a leading academic institution in the study of conflict resolution, peacebuilding, and security. The department is renowned for its research and education programs aimed at fostering a deeper understanding of conflict dynamics and peace processes. This department also hosts the [Uppsala Conflict Data Program (UCDP)](https://ucdp.uu.se/), a central data source for the VIEWS project. About half of the VIEWS core team is currently located at Uppsala University .


### Our Partners 

