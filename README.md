# Bike Share Station Rebalancing Minimization

## Overview

Bike Share Toronto allows a rider to rent a bike from one of its 680 stations and return that bike to any station in the network. As some of these stations are more popular ride starting locations vs. ride ending locations (and vice versa), Bike Share Toronto needs to expend resources on rebalancing these stations to ensure that riders don't come across stations that are full or empty. In order to be useful to riders, each station in the network needs to have bikes available to rent, as well as spaces available for docking. To solve this problem, Bike Share Toronto uses trucks to drive bikes from full stations to empty ones. This task of rebalancing is taxing on Bike Share Toronto's operating budget. For this reason, it would be beneficial to Bike Share Toronto to know how much of a burden a new station would be on its rebalancing team, before installing that station.

## Project Goal

The goal of this project is to create a tool that can predict a proposed Bike Share Toronto station's burden on the rebalancing team, using the proposed station's longitude, latitude, and elevation.

Note that this tool is not intended to be a sole decision-maker for planning station additions. There are many factors that should be considered when adding a new station to the network, such as the station's projected usage and cost of installation. For example, it's easy to imagine why Bike Share Toronto would want to add a station to a very highidemand area, even if that proposed station would require rebalancing—the income generated from that station could, potentially, pay for its own rebalancing. Nonetheless, this rebalancing minimization tool would still provide decision-makers with helpful information.

## Project Timeline

### Phase 1: Data Collection [In Progress]
File: (coming soon)\n
Ride data (originally downloaded as .csv files), station data (.json), and elevation data (.tif) will be combined and exported as a parquet file. Columns will be cast down to memory-efficient data types before exporting.

### Phase 2: Data Visualization
File: (coming soon)
Data will be analyzed, visually, using maps and scatter plots. A dashboard, displaying several city maps, will be created using Plotly.

### Phase 3: Machine Learning Model
File: (coming soon)
A linear regression model will be trained using a station's longitude, latitude, and elevation as predictor variables, and the station's ride-end ratio (# of rides ended at the station / # of rides started or ended at the station) as the target variable.

### Phase 4: Review/Next Steps
File: (coming soon)
Strengths and limitations of the rebalancing minimization tool will be discussed, as well potential future projects that this project can be used as a steppingstone towards.