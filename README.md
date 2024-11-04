# Somersaulting to Gold: Optimizing USA’s Artistic Gymnastics Team Selection Strategy

## Overview

This repository contains the analysis and simulation code for optimizing the selection of the U.S. Artistic Gymnastics teams for the 2024 Paris Olympics. Our project presents a simulation-based methodology that leverages historical data to assess different team compositions and maximize medal potential.

## Motivation

Gymnastics is one of the most anticipated Olympic events in the U.S., fueled by past successes like the "Final Five" in 2016 and standout athletes such as Simone Biles. As the U.S. Olympic Committee prepares to select the 2024 team, assembling a data-driven strategy to optimize team composition is crucial. This repository offers a simulation model that aims to support these efforts by analyzing potential outcomes for both individual and team events.

## Methodology

### Data Collection
- **Sources**: The dataset includes the 2022-2023 season's results for male and female gymnasts from various competitions, supplemented by additional data obtained through web scraping.
- **Cleaning**: Missing or zero scores were removed, and data consistency checks were performed, including correcting athlete names and national affiliations.

### Simulation Approach
- **Kernel Density Estimation (KDE)**: Used to estimate score distributions for each athlete-apparatus combination. This approach allows for near-continuous modeling of gymnastic scores and accommodates variability in the data.
- **Iterations**: We ran 1,000 iterations for simulations of each event (4 for women, 6 for men) to generate robust datasets reflecting possible outcomes.

### Medal Scoring System
- **Weighted Scoring**: Assigns gold, silver, and bronze medals with scores of 3, 2, and 1, respectively. Scores below bronze receive 0. The average weighted score across simulations reflects each athlete’s medal potential.

## Results

### Top Performers and Team Analysis
- **Women's Team**: Simone Biles emerged as the top contributor across all apparatuses, followed by Konnor McClain and Shilese Jones.
- **Men's Team**: Brody Malone and Fred Richard were identified as key team members, with the simulation indicating varied optimal team combinations.
- **Team Events**: The simulations showed that certain combinations, particularly those including Biles, were most likely to achieve gold.

## Key Findings
- The U.S. has strong potential in events like the floor and vault for women, while apparatuses like the uneven bars remain competitive internationally.
- For men, a focus on generalists, such as Malone, paired with specialists can increase the likelihood of winning a team medal for the first time since 2014.

## Limitations
- **Data Gaps**: Collegiate competition data was limited, potentially affecting the accuracy for athletes with significant NCAA experience.
- **Model Assumptions**: The model assumes independence between rounds and uses scores equally weighted across events, which may not reflect in-practice conditions like fatigue or performance trends.

## Future Work
- Incorporating weighted scores by competition recency and scope.
- Adding fatigue parameters for multi-event participation.
- Validating simulations with past event data for model refinement.
