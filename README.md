# Deep-Convolutional-Q-Learning-for-Pac-Man
This repository implements Deep Convolutional Q-Learning (DQN) for playing the classic Pac-Man game. 
The DQN approach combines reinforcement learning with deep learning to teach an agent how to play Pac-Man by maximizing its score through strategic decision-making. The agent learns to navigate the game environment by interacting with it and optimizing future rewards.

Key Features:
  Convolutional Neural Networks (CNNs): The model uses CNNs to process the visual input (game screen), extracting features relevant to decision-making in Pac-Man.
  Q-Learning: The Q-learning algorithm is applied to learn the value of actions (e.g., moving in different directions) given the current game state.
  Experience Replay: Stores past experiences to break the correlation between consecutive game steps and improve learning stability.
  Target Network: A secondary, periodically updated network is used to stabilize learning and avoid excessive Q-value oscillations.
Structure:
  Training Environment: The Pac-Man game environment, where the agent learns from reward signals based on eating pellets, avoiding ghosts, and other in-game objectives.
  Model Architecture: A CNN processes frames of the game, followed by fully connected layers that estimate the Q-values for each possible action.
  Training Loop: The agent interacts with the environment, collects experiences, updates the Q-network using the Bellman equation, and periodically updates the target network.
How It Works:
  The agent observes the game screen as raw pixel input.
  The CNN extracts features from the screen and predicts Q-values for each action (move left, right, up, down).
  Using an ε-greedy policy, the agent chooses actions to explore the environment or exploit learned behaviors.
  Over time, the agent learns optimal strategies to maximize its cumulative reward in Pac-Man, learning to avoid ghosts, collect pellets, and chase fruit.
Dependencies:
  Python 3.x
  TensorFlow/PyTorch (for deep learning)
  OpenAI Gym or custom Pac-Man environment
