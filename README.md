# FaultTolerantTaskOffloadingSimulation
This project proposes a DRL-based fault-tolerant task offloading method for Mobile Edge-Cloud Computing. Using a DDPG algorithm, it minimizes latency and enhances reliability for delay-sensitive tasks in dynamic environments while adapting to resource fluctuations and failure rates.
# User Guide for the Simulator



Before starting, please ensure that you have installed the following libraries:

Python version: **3.7.16**

The following libraries are utilized in the simulator:

itertools: Provides functions for creating iterators for efficient looping.
scipy.stats: Contains statistical functions, including probability distributions.
pandas: A data manipulation and analysis library, ideal for handling data structures.
random: Implements pseudo-random number generators for various distributions.
configuration: Imports parameter configurations specific to the simulation.
numpy: A library for numerical computations, offering support for large, multi-dimensional arrays and matrices.
truncnorm: From scipy.stats, it is used for truncated normal distributions (in ddpg.py).
tensorflow: An open-source machine learning library used for building and training models.
keras: A high-level neural networks API that runs on top of TensorFlow.
simpy: A process-based discrete-event simulation framework.
params: Imports parameter definitions specific to the simulation.
math: Provides mathematical functions.
os: Provides a way of using operating system-dependent functionality.
openpyxl: A library for reading and writing Excel files, used here for managing results.
Image and BarChart: From openpyxl.drawing.image and openpyxl.chart, respectively, for handling images and creating charts in Excel files.



## Starting the Simulation

To begin the simulation, you first need to run the following file to generate parameters related to tasks and servers:

- `generate_server_and_task_parameters.py`

Then, navigate to the Proposed Approach subfolder and execute the following file in the VSCode environment:

- `ddpg_main.py`

### Configuring Scenarios

To run scenarios for high and low failure rates, simply set the `permutation_numbers` in the `ddpg_main.py` file as follows:

- For low failure rate: `permutation_numbers = [1]`
- For high failure rate: `permutation_numbers = [3]`

## Simulator Features

The simulator is designed to support the execution of homogeneous and heterogeneous scenarios, as well as high, low, and medium failure rates. Additionally, the code allows for switching between different failure modes.

Finally, after successfully running the simulation, results will be saved in the **Homogeneous_Results** or **Heterogeneous_Results** folders based on the executed scenario.

## Citation
If you use this code, please cite the corresponding paper:
Babaiyan, V., Bushehrian, O. A deep-reinforcement-learning-based strategy selection approach for fault-tolerant offloading of delay-sensitive tasks in vehicular edge-cloud computing. J Supercomput 81, 708 (2025). https://doi.org/10.1007/s11227-025-07196-9

## License
MIT License

