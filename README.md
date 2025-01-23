# Percolation in Random Graphs: An Experimental Study

*This is a repository containing part of the code used in the final assignment of the Complex Networks course in the University of Twente (Master of Applied Mathematics, Fall 2022).*

<img src="percolation.gif" alt="Percolation" width="500">

## Introduction

This study explores the phenomenon of percolation in random graphs, specifically focusing on the Erdős-Rényi model.
The main goal of this final assignment was to investigate the percolation transition in Erdős-Rényi random graphs, focusing on the nature of the transition between subcritical and supercritical states. Specifically, the study aimed to:

- Empirically investigate the percolation transition in Erdős-Rényi random graphs, examining how the network's structural properties change as edges are systematically added or removed.
- Examine the behavior of the maximum component size during the percolation process.


## Background

### Random Graphs

Random graphs are mathematical structures consisting of a set of vertices connected by edges, where the connections are determined by some random process. They serve as important models for complex networks in various fields, from social networks to biological systems.

### Erdős-Rényi Model

The Erdős-Rényi model, named after mathematicians Paul Erdős and Alfréd Rényi, is a simple yet powerful method for generating random graphs. In this model, edges are added between vertices with a fixed probability, independent of other edges.

### Percolation Theory

Percolation theory studies the formation and properties of connected components in random graphs. More specifically, it examines the behavior of connected clusters in random graphs as edges are added or removed. Of particular interest is the emergence of a giant component, which occurs when a significant fraction of the graph becomes connected.

## Methodology

Our experiment employs Python to simulate and analyze percolation in Erdős-Rényi graphs. We utilize the following key libraries:

- NetworkX for graph generation and manipulation
- NumPy for numerical computations
- Plotly for data visualization

The core of our analysis revolves around two main functions, which we've integrated into a comprehensive approach:

1. `erdos_renyi_percolation(n, lamda)`: This function generates an Erdős-Rényi graph and simulates the percolation process.

2. `er_percolation_plot(n, lamda)`: This function creates a visualization of the percolation process, plotting the relative size of the largest component (C/n) against the fraction of edges present (r).

### Key Aspects of Our Approach:

- We first generated the Erdős-Rényi graph using the built-in function of the NetworkX library.
- Instead of adding edges one by one, we started with the generated graph and systematically removed edges. This approach was chosen for its computational efficiency and allowed us to experiment with different values of λ.
- The percolation process is simulated by randomly removing edges from the initial graph.
- We measure the maximum component size as a function of edge density throughout the edge removal process.
- The transition point where the maximum component size changes dramatically is analyzed to understand the nature of the percolation transition.

This methodology allows us to efficiently explore the percolation dynamics in Erdős-Rényi graphs while providing flexibility in our experimental parameters.

## Results and Discussion

The experiment reveals a critical phenomenon in percolation: the sudden emergence of a giant component. As edges are added to the graph, there comes a point where the size of the largest connected component abruptly increases, transitioning from small, isolated clusters to a single large cluster that spans a significant portion of the graph.

This phase transition is visualized in our plots, where we observe:

1. A sharp increase in the relative size of the largest component (C/n) at a critical point.
2. The asymptotic approach of C/n to a value known as the survival probability (ζ) as r increases.

The survival probability, calculated using the `zeta_l(lamda)` function, represents the fraction of vertices that belong to the giant component in the limit of large graph size.

### Animated Visualization

To provide a more intuitive understanding of the percolation process, we generated an animated video simulating the exact process of percolation and its effect on the graph. This animation visually demonstrates:

- The gradual addition of edges to the graph
- The formation and growth of connected components
- The emergence and expansion of the giant connected component
- The dynamic changes in graph structure throughout the percolation process

This animated visualization serves as a powerful tool for observing and understanding the critical transition in percolation, complementing our quantitative analysis and static plots. It allows us to visually track the evolution of the graph's connectivity and the dramatic shift that occurs at the percolation threshold.

## Conclusion

Our experimental study of percolation in Erdős-Rényi graphs demonstrates the sudden emergence of a giant component as the number of edges increases. This phenomenon, characteristic of phase transitions in complex systems, has profound implications for understanding connectivity in various real-world networks.

Future work could extend this analysis to other random graph models or explore the impact of different edge removal strategies on the percolation process.


