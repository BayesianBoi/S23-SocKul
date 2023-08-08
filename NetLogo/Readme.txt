NetLogo Social Network Contagion Model
This repository contains a NetLogo model that simulates the spread of contagion in a social network. The model allows users to create various types of networks and investigate the dynamics of contagion within them. The contagion can be initiated from a set of seed nodes, and its spread is influenced by parameters such as diffusion probability and seeding method.
Setup
Before running the model, ensure that you have NetLogo installed on your system. To execute the simulation, follow these steps:
1. Open NetLogo and load the model file.
2. Click the "Setup" button to initialize the simulation environment and create the social network based on the chosen network type.
3. Set the desired parameters, such as the number of nodes, network type, seeding method, diffusion probability, and others.
4. Click the "Go" button to start the simulation.


Global Variables

The model utilizes several global variables to track and calculate network measures during the simulation. Some of the key global variables include:

* mean-path-length: Average path length between nodes in the network.
* adopter-size-list: Percentage of infected nodes (adopters) in the network.
* active-agents: A set of nodes that are currently active in spreading contagion.
* network-density: Density of the social network.
* avg-clustering-coef: Average clustering coefficient of nodes in the network.
* avg-degree: Average degree of nodes in the network.
* max-deg: Maximum degree among nodes in the network.
* min-deg: Minimum degree among nodes in the network.
* modularity: Modularity of the network, calculated using Louvain community detection algorithm.
* network-diameter: Diameter of the network.
* seed-nodes: A set of nodes chosen as seed nodes for contagion initiation.



Each node (turtle) in the network has several variables, including:
* adopt?: A boolean variable indicating whether the node has been infected with contagion.
* clustering-coefficient: Defines the likelihood that two randomly selected neighbors of a node are neighbors themselves.
* has-spread?: A boolean variable indicating whether the node has attempted to infect its neighbors.
* degree: The degree of the node, representing the number of connections it has.
* influence: An influence measure calculated from the k-shell degree.
* dis-degree: A discounted degree used in the degree discount heuristics.
* ks-degree: The k-shell degree of the node, used in the k-shell seeding method.
* nb-seed-neighbors: Number of neighbors of the node that are already selected as seed nodes.
* eigenvector-centrality: Eigenvector centrality measure for the node.



The model includes several procedures to handle different aspects of the simulation:

* setup: Initializes the simulation by clearing the environment, creating the social network, and setting up seed nodes.
* generate-network: Generates the social network based on the chosen network type.
* spread-seed-nodes: Initiates contagion by selecting seed nodes based on the chosen seeding method.
* degree-discount: Implements the degree discount heuristics for seed node selection.
* k-shell: Implements the k-shell seeding method based on k-shell decomposition.
* initialize-turtle: Initializes the properties of each node (turtle).
* calculate-network-measures: Calculates various network measures such as degree, clustering coefficient, and modularity.
* go: The main procedure for running the contagion simulation, which handles the spread of contagion and updates node colors.
* calculate-adopter-size: Calculates the percentage of infected nodes (adopter size) in the network.
* update-color: Updates the color of nodes based on their infection status.
* layout: Performs network layout using the spring layout algorithm.
* community-detection: Detects communities using the Louvain community detection algorithm.
* color-clusters: Colors nodes and links according to their assigned communities.

