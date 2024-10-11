# Bayesian Q-Learning for Maze Navigation

![image](https://github.com/user-attachments/assets/0eec83d4-916e-4592-8042-a000c66b5e2d)

![image](https://github.com/user-attachments/assets/08ac2ded-3307-4815-8be9-e3bc1f67fc88)

![image](https://github.com/user-attachments/assets/a8d65b6b-c5b3-4415-92b6-36caf213692d)

![image](https://github.com/user-attachments/assets/abee1491-ca24-432a-a5fd-c91b5ee0e615)

![image](https://github.com/user-attachments/assets/5fea7eef-973c-4087-978e-9cc589de2fe9)

![image](https://github.com/user-attachments/assets/68d7bf66-7381-4ab6-9f6f-519ceb6dcc73)

![image](https://github.com/user-attachments/assets/6d087c97-b3a8-4dce-bbc4-aa74ebc5ff7c)

![image](https://github.com/user-attachments/assets/e7e15a86-313a-4580-a811-707290199700)



This project implements a Bayesian Q-Learning algorithm to solve a maze navigation problem. The agent learns to find the optimal path from the start to the goal in a 2D maze environment, using a Bayesian Neural Network to approximate Q-values.

## Features

- Bayesian Neural Network for Q-value approximation
- Population coding for state representation
- Thompson sampling for exploration
- Comprehensive visualization and analysis tools

## Requirements

- Python 3.7+
- PyTorch
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/bayesian-q-learning-maze.git
   cd bayesian-q-learning-maze
   ```

2. Install the required packages:
   ```
   pip install torch numpy matplotlib seaborn scikit-learn
   ```

## Usage

1. Run the main script:
   ```
   python bayesian_qlearning.py
   ```

2. The script will train the agent and generate various visualizations to analyze the learning process and the trained model.

## Model Architecture

The Bayesian Q-Learning model uses a two-layer Bayesian Neural Network:

- Input layer: 25 neurons (population coding of the 2D state)
- Hidden layer: 64 neurons
- Output layer: 4 neurons (Q-values for Up, Right, Down, Left actions)

Each layer uses a mean and standard deviation for weights, allowing for uncertainty estimation.

## Key Components

1. `BayesianQLearning`: The main model class implementing the Bayesian Neural Network.
2. `Maze`: The environment class representing the 2D maze.
3. `population_coding`: Function to encode the 2D state into a population code.
4. `bayesian_q_learning`: The main training loop implementing the Q-learning algorithm.
5. `analyze_trained_model`: Comprehensive analysis function generating various visualizations.

## Visualizations

The project includes several visualizations to help understand the learning process and the trained model:

1. Cumulative Reward per Episode
2. Success Rate
3. Agent Path
4. Q-value Maps
5. Learned Policy and Uncertainty
6. Q-value Distributions
7. PCA and t-SNE of Neural Activities
8. Receptive Fields
9. Weight Distributions
10. 3D Neural Manifold
11. Neuron Direction Preferences
12. Hidden Layer Activation Patterns

## Customization

You can customize the maze layout, learning parameters, and model architecture in the main script. Adjust the following variables to experiment with different settings:

- `maze`: The layout of the maze (0 for free space, 1 for walls)
- `num_episodes`: Number of training episodes
- `alpha`: Learning rate
- `gamma`: Discount factor
- `initial_epsilon`, `min_epsilon`, `decay_rate`: Exploration parameters

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

This implementation is inspired by recent advancements in Bayesian Deep Learning and Reinforcement Learning. It combines ideas from Thompson Sampling, Population Coding, and Bayesian Neural Networks to create a robust learning algorithm for maze navigation.
