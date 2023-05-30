# Bike Share Station Rebalancing Minimization

## Overview

Bike Share Toronto allows a rider to rent a bike from one of its 680 stations and return that bike to any station in the network. As some of these stations are more popular ride starting locations vs. ride ending locations (and vice versa), Bike Share Toronto needs to expend resources on rebalancing these stations to ensure that they do not become full or empty. In order to be useful to riders, each station in the network needs to have bikes available to rent, as well as spaces available for docking. To solve this problem, Bike Share Toronto uses trucks to drive bikes from full stations to empty ones. This task of rebalancing is taxing on Bike Share Toronto's operating budget. For this reason, it would be beneficial to Bike Share Toronto to know how much of a burden a new station would be on its rebalancing team, before installing that station.

## Project Goal

The goal of this project is to create a tool that can predict a proposed Bike Share Toronto station's burden on the rebalancing team, using the proposed station's longitude, latitude, and elevation.

Note that this tool is not intended to be a sole decision-maker for planning station additions. There are many factors that should be considered when adding a new station to the network, such as the station's projected usage and cost of installation. For example, it's easy to imagine why Bike Share Toronto would want to add a station to a very high-demand area, even if that proposed station would require rebalancing—the income generated from that station could, potentially, pay for its own rebalancing. Nonetheless, this rebalancing minimization tool would still provide decision-makers with helpful information.

## Project Timeline

### Phase 1: Data Collection [Complete]
Ride data (originally downloaded as .csv files), station data (.json), and elevation data (.tif) are combined and exported as a parquet file. Columns are cast down to memory-efficient data types before exporting.  
  
File: [data.ipynb](https://github.com/stephensavoia/rebalancing_minimizer/blob/main/data.ipynb)

### Phase 2: Data Visualization [Complete]
Data is analyzed, visually, using maps and scatter plots.

File: [visualization.ipynb](https://github.com/stephensavoia/rebalancing_minimizer/blob/main/visualization.ipynb)

### Phase 3: Machine Learning Model [Complete]
A model is trained using a station's longitude, latitude, and elevation as predictor variables, and the station's ride-end ratio (# of rides ended at the station / # of rides started or ended at the station) as the target variable.

File: [model.ipynb](https://github.com/stephensavoia/rebalancing_minimizer/blob/main/model.ipynb)

### Phase 4: End-Ratio Geographic Heat Map [In progress]
A final geographic heat map of Toronto will be created, showing areas where ride-end ratio will be high vs. low. Bike Share Toronto network planners can use this map to anticipate a new station's ride-end ratio (and, therefore, its burden on the rebalancing team).

### Phase 5: Review/Next Steps
Strengths and limitations of the rebalancing minimization tool will be discussed, as well potential future projects that this project can be used as a steppingstone towards.