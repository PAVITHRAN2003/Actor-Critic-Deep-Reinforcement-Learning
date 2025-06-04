This README details a Reinforcement Learning project focused on implementing the Advantage Actor-Critic (A2C) algorithm across various Gymnasium environments.

Project Overview
The project is structured into three main parts, along with an optional bonus section:

Part I: Actor-Critic Fundamentals

Neural Network Architectures: Implementation of separate and shared actor-critic networks, with discussions on their motivations.
Dynamic Network Generation: A create_shared_network(env) function that dynamically builds actor-critic networks for different Gymnasium environments, handling various observation and action spaces.
Observation Normalization: A normalize_observation(obs, env) function to scale observations to [-1, 1] for bounded Box spaces.
Gradient Clipping: Demonstration of torch.nn.utils.clip_grad_norm_ for stabilizing training.
Part II: A2C/A3C Implementation

Algorithm: Implementation of the A2C algorithm, a synchronous variant of A3C, utilizing at least two actor-learner threads.

Multi-threading: Details on how threads collect experience independently and synchronize gradients for global model updates using Python's multiprocessing or torch.multiprocessing.

Environment & Results: Training on CartPole-v1. The report includes discussions on actor and critic roles, the importance of the "advantage" function, and loss functions used. Training and evaluation plots illustrate the agent's learning progression and performance.




Part III: Complex Environment Solutions

Environments: Application of the A2C algorithm to BipedalWalker-v3 and LunarLander-v3. Environment details, including state and action spaces, goals, and rewards, are described.


Results: Training plots show reward per episode for both environments, comparing algorithm behavior. Evaluation results for each environment are also provided.

Bonus Part: MuJoCo Environment

Environment: The A2C algorithm was applied to the InvertedPendulum-v5 MuJoCo environment.
Analysis: A reward plot demonstrates the learning curve. The implemented algorithm and challenges encountered during training are discussed.



Repository Contents
Jupyter Notebooks for each part: a3_part_1_UBIT1_UBIT2.ipynb, a3_part_2_UBIT1_UBIT2.ipynb, a3_part_3_UBIT1_UBIT2.ipynb, a3_bonus_mujoco_UBIT1_UBIT2.ipynb.


Project report: a3_report_UBIT1_UBIT2.pdf.

Saved model weights (e.g., .h5, .pth, or .pickle files) for trained models.



Evaluation videos/screenshots (if applicable).

Setup & Run
Clone the repository.
Install required libraries (e.g., gymnasium, torch).
Run the Jupyter Notebooks to see results and plots.
