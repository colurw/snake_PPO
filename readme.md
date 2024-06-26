# snake_PPO

A work in progess....

Proximal Policy Optimisation is a state-of-the-art reinforcement learning algorithm designed to allow gradient learning methods to be applied to situations where an 'intelligent' agent makes autonomous decisions in an environment.  This permits a back-propogation of the environment's gradients through the network (effectively) after each decision.  

This (theoretically) should speed up the learning process when compared to gradient-free methods, such as <a href="https://github.com/colurw/flight_sim_GNN" title="colurw/flight_sim_GNN">flight_sim_GNN</a>, which suffer through a randomised exploration of the environment's reward manifold.  

### snake_cli.py
Is an ascii version of the classic Nokia mobile game, playable in the command line using keyboard controls, that captures screen and keypress datastreams.  Intended for a supervised learning project, that was abandoned after realising that I didn't want to spend hours playing it to create the data.  Hence...

### snake_pyg_num.py
Deprecates the data capture, and transforms the output into a RGB image array, and uses PyGame to generate a more attractive display window.

### snake_gym.py
Refactors the game into a Gymnasium Environment() to simplify integration with reinforcement learning algorithms.

### PPO.py
Initialises a convolutional neural network that learns how to use the control inputs, based on its interpretation the RGB screen array.

### To Do
* ~~Customise CNN policy to suit smaller screen.~~
* Integrate with 'Weights And Biases' or Tensorboard to aid with determining proper hyperparameters
* Capture PyGame screens to show learning progress over many epochs.
