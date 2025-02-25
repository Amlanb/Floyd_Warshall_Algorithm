# Airport Connectivity Analysis using Floyd-Warshall Algorithm

# Overview

This project analyzes airport connectivity using graph theory, specifically the Floyd-Warshall Algorithm for shortest path computation. The dataset includes airports, runways, and navigational aids, which are processed to construct a global airport network and evaluate connectivity.

# Project Objectives

  Construct an airport network using real-world geospatial data.
  Implement the Floyd-Warshall Algorithm to compute the shortest paths between airports.
  Identify most central and most isolated airports based on shortest path metrics.
  Perform network analysis (density, clustering coefficient, degree distribution, etc.).
  Visualize results using geospatial heatmaps and centrality comparisons.

# Dataset Used

  Airports Data (Location, country, and identifiers)
  Runways Data (Lengths, airport association)
  Navaids Data (Navigation aids for airports)
  Geospatial Coordinates (Latitude, longitude for visualization)

# Key Learnings

1. Network Connectivity Issues

The initial 500 km threshold led to a disconnected network, resulting in infinite shortest path values.
Increasing the threshold or using actual flight route data improves connectivity.

2. Centrality Insights

Central airports should have the shortest average path to others, but disconnected nodes skew results.
The most connected airports (hubs) play a vital role in efficient global air travel.

3. Graph Theory in Real-World Applications

Floyd-Warshall Algorithm efficiently finds all-pairs shortest paths but is computationally expensive.
Degree Distribution and Closeness Centrality highlight regional and global hubs.

# Visualizations

  Heatmaps of Airport Connectivity based on geospatial data.
  Degree Distribution Plot to understand connectivity patterns.
  Closeness vs. Betweenness Centrality scatter plots for network insights.


# Key Conclusions from the Analysis:

# Network Density:
The airport network has a low density of 0.015, indicating that only about 1.5% of all possible airport connections exist. This suggests a sparse network with many airports not directly connected.

# Clustering Coefficient:
The average clustering coefficient is 0.576, meaning that airports tend to form local clusters where direct neighbors are also interconnected. This implies regional hubs or country-based connectivity.

# Central Airports (Most Connected):
The central airports should ideally have the shortest average shortest path to all other airports. However, the results show infinity (inf) values, which suggests that the network is disconnected, and many airports do not have a path to all others.

# Isolated Airports:
The same set of airports appears under "Most Isolated Airports," again with inf values, confirming that they are not connected to the network properly. This might be due to an issue in defining connections or an overly strict distance threshold.
