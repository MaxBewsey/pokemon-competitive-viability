# A Machine Learning Approach to Competitive Viability in Pokémon VGC

## Overview
This capstone project explores what makes a Pokémon competitively viable in the official Video Game Championships (VGC) format. Using features such as base stats, typings, and abilities, I built a predictive neural network and an interactive tool that estimates viability for both existing and hypothetical Pokémon.

## Key Features
- Curated dataset of all 1025 Pokémon (stats, typings, evolutions, Worlds winners)
- Exploratory Data Analysis:
  - Base stat distributions by generation, typing, Legendary status
  - Typing frequencies, dual-type heatmaps
  - Ability usage
  - PCA + K-Means clustering to identify archetypes
- Worlds Winners Analysis:
  - Compared traits of winners vs. the general population
- Predictive Modelling:
  - Neural network classifier built in PyTorch
  - Probability of Worlds success based on traits
- Interactive Viability Rater:
  - Adjust stats with sliders
  - Select typings and abilities
  - Visualise results on radar plot
  - Compare to similar Pokémon using Nearest Neighbour logic.

## Methods & Tools
- **Data Engineering & Cleaning:** pandas, numpy, dataset merging, feature engineering  
- **Visualisation:** matplotlib, seaborn, radar charts, heatmaps, bar plots, box plots, lollipop plots  
- **Clustering & Dimensionality Reduction:** PCA, K-Means
- **Modelling:** PyTorch neural network classifier
- **UI Development:** ipywidgets
- **Similarity Search:** scikit-learn NearestNeighbors

## Repo Structure
- data/
  - Pokemon Database
  - evolutions
  - VGC World Championship Winners
- images/
  - charizard
  - type_chart
- notebooks/
  - A Machine Learning Approach to Competitive Viability in Pokémon VGC
- README.md


## Results
- Confirmed that **stats, typings, and abilities alone are highly predictive** of competitive viability at the World Championship level.  
- Identified clear patterns in winners:
  - **Legendaries, dual typings, and top-tier abilities** (e.g., Intimidate, Levitate) are strongly overrepresented.  
  - Legendary Pokémon make up over **40% of Worlds winners**, despite representing a much smaller share of the population.  
- Neural network model achieved strong predictive performance:
  - Precision = 0.909  
  - Recall = 0.714  
  - PR-AUC = 0.749  
- Demonstrated that the model implicitly learns **legality and metagame context**:
  - High-BST Legendary/Mythical Pokémon are penalised, reflecting their historical ineligibility for Worlds.  
- Built an **interactive Viability Rater** tool:
  - Generates predicted probability of success for existing or hypothetical Pokémon.  
  - Visualises design with radar plots and typing/ability displays.  
  - Compares designs to their five most similar real Pokémon.  
