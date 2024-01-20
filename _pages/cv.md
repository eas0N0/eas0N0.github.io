---
layout: archive
title: ""
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

# Education
The Chinese University of Hong Kong, Shenzhen (2020-2024)
  
  _Bsc in Data Science and Big Data Technology_


# Professional Experience

**Tencent Ltd.**
_Algorithm Engineer Intern, Machine Learning Platform Department_  
06/2023 - 09/2023  
Shenzhen, China

* Contributed to support the advancement of Tencent’s flagship Large Language Model (LLM), concerning the Reinforcement Learning with Human Feedback (RLHF) and Supervised Fine-tuning (SFT)
* Enhanced the performance of the Proximal Policy Optimization (PPO) reinforcement efficacy for LLM; Implemented pre-processing on input prompts to mitigate the negative impact of homogeneous prompts on reinforcement effects
* Completed the investigation for appropriate mining methods and distance metrics of prompt text to strike a balance between data volume and diversity; Developed a framework for maintaining diversity within the prompts’ pool based on the research
* Established Prompt Learning paradigm for the LLM’s reinforcement, including mining, cleaning, labeling, and classification of prompt data based on self-instruct methods and open-source dataset mining
* Executed recall task for misclassified prompts, employing classification methods of Ensemble Learning, Fine-tuned BERT, Graph Convolutional Network (GCN) and Graph Attention Network(GAT), achieving a final F1-score of 0.88


**Shenzhen Research Institute of Big Data** 

_Research Assistant_

03/2023 - 07/2023

Shenzhen, China
* Developed a Markov transition model to predict time series trajectories of students, optimizing campus resource allocation
*	Extracted location data from device-connected WLAN data; Performed processing such as anomaly detection, missing value imputation, and time series segmentation on raw trajectory data to enhance data quality and usability
*	Applied DTW distance and Fréchet distance metrics and utilized clustering algorithms, including K-means, DBSCAN, and hierarchical clustering, to cluster trajectory sequences, in order to improve predicting accuracy
*	Derived the decay relationship of prediction accuracy with increasing time spans and achieved a maximum accuracy of 0.77 for position prediction after 1 hour and 0.67 after 15 hours 
* Optimized school bus scheduling and managing nighttime classroom openings based on trajectory prediction results; Reduced nighttime electricity costs by 4.8%

**Shenzhen Intellifusion Technologies Co. Ltd.**

_Big Data Engineer Intern, Big Data Department_

06/2022 - 08/2022

Shenzhen, China
*	Developed three time-series forecasting models to predict bus passenger flow, considering both route and time-of-day dimensions; Explored predictive stability by continuous decreasing route scale and increasing time granularity
*	Processed more than six hundred million rows of bus pass transaction records; Enhanced prediction accuracy through hyperparameter tuning and ensemble learning techniques; Achieved the lowest MAPE for daily prediction at 0.014
*	Applied the models to enhance the company’s Bus Simulation Optimization System to improve the bus resource allocation; Reduced the daily operational costs for 6.9% and average passenger waiting times for 5.2% based on the forecasting results
*	Derived probability distributions for individual passengers across various travel times and routes


  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Currently signed in to 43 different slack teams
