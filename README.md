# Simulation and Analysis of Percolation Systems

The Jupyter Notebook `percolation-5-12-2023.ipynb` in this repository contains my active work on the simulation and analysis of percolation systems.

[Percolation systems](https://en.wikipedia.org/wiki/Percolation_theory) are often used to model physical phenomena such as spin networks and pandemic outbreaks. 
There are many types of percolation systems, and I choose to focus first on percolation in a 2-dimensional grid.  

The familiar game of "[Dots and Boxes](https://en.wikipedia.org/wiki/Dots_and_boxes)" provides a good analogy. On a 2-dimensional grid of nodes, links can be added to
neighboring nodes (up, left, right, and down). In these percolation systems, connections are added at random, with independent probability `p`. For example, if `p` = 0, no connections
will be present. At `p` = 0.3, every possible connection has a 30% chance of being added. And at `p` = 1, all of the connections are added.  

The system becomes interesting when we begin to analyze the formation of clusters, or groups of connected nodes. At `p` = 0, each node is its own cluster. At `p` = 0.3, some small clusters
have formed. And at `p` = 1, there is one giant cluster. It is a well-established fact in percolation theory that the 2-dimensional system undergoes a phase transition at the critial `p` = 0.5.
When each possible connection has a 50% chance of being added, the system shows fractal structure, exhibiting scale invariance in the shapes and sizes of clusters. See `critical_percolation.png` to preview a 1000x1000 critical system. 

In this project I generate and visualize percolation systems. I make use of interavtive sliders to more intuitively see the effects of changing `p` and easily view only the `n` largest clusters.
I visualize the cluster size distributions near criticality to show the existence of a phase transition at `p` = 0.5. Next, I perform least-squares regression to fit curves to various distributions
describing the clusters sizes. I use these models to again show the existence of a phase transition. This can also be used to predict the size of the largest cluster and the overall distribution of cluster sizes given `p`.  

Most recently, I trained a Convolutional Neural Network to recognize `p` simply by looking at an image of the percolation system. As of now, my best model correctly identifies the `p`-value of unseen percolation images with 4.2% error. This can be used to detect phase transitions. 

Future work includes the detection of scale invariance, generalizing the system to an arbitrary network, and using this to model social network and pandemic outbreak data. A very similar model could potentially be used to predict the course of future pandemic outbreaks by identifying clusters and phase transitions on social networks.

Thanks to Professor Vladimir Lukic at Stevens Institute of Technology for project advice.
