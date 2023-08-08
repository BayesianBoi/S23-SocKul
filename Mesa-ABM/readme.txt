
Agent-Based Model for Opinion Dynamics

This repository contains a Python script for ABM that simulates opinion dynamics in a social network. The model explores how individual agents form and update their opinions based on interactions with their neighbors in the network.


The following Python packages are required to run the script:
* Mesa: The primary package used for Agent-Based Modeling. You can install it using pip with !pip install mesa.

* Matplotlib: Used for plotting the simulation results. You can install it using pip with !pip install matplotlib.


The model consists of two classes: MyAgent and MyModel.

MyAgent represents individual agents in the social network. Each agent has the following attributes:
* opinion: A static opinion on a given topic, either 0 (for negative) or 1 (for positive).
* willingness_to_self_censor: A static willingness to self-censor, drawn from a uniform distribution [0, 1].
* confidence: The agent's confidence in its opinion, which changes throughout the iterations.
* previous_speaks_out: A boolean indicating whether the agent spoke out in the last iteration.

The agent has methods to calculate its confidence based on the opinions of its neighbors and to decide whether to speak out based on its confidence.

MyModel represents the entire simulation model. It includes parameters such as the number of agents (N), the number of edges to attach from a new node to existing nodes (m) in the Barabasi-Albert scale-free network, and the degree distribution of the network (y).

The model creates a Barabasi-Albert scale-free network and populates it with MyAgent instances. The agents interact with their neighbors in each iteration, updating their confidence levels and deciding whether to speak out. The simulation continues until a stable state is reached (defined by agents' confidence differences being smaller than a threshold) or a maximum number of iterations (ticks) is reached.



To run a single simulation, you can modify the parameters (N, m, y, and ticks) and then execute the script.
For multiple simulations with varying m values, the script runs multiple simulations for each m and records the results in a CSV file named "results.csv". The CSV file includes data on agent opinions, speaking status, percentages of opinions, the majority opinion, the central node's opinion, and more.

