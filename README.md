# CarRacingImitationLearning
A very interesting approach to Imitation learning : 
CarRacing-v0:

Actions:
    Steering: real valued in [-1, 1]
    Gas: real valued in [0, 1]
    Break: real valued in [0, 1]

Observations:
   STATE_W = 96  * STATE_H = 96 * 3 : RGB Image  

Image obervations are the only input, the reward is just indicative.


- CarConfig.py:
Global config

- CarRacing_Play.py:
Plays open AI gym CarRacing-v0 and stores observations and actions

- CarRacing_Learn.py: 
Trains Convolutional Neural Network (see Keras model.png) on saved data

- CarRacing_Imitate.py: 
Load tained model, wrangles observations, predicts actions and simulate environment

- Demo.mp4: 
One of the decent results. 
The algorithm revealed very sensitive to hyperprameters. The learned self-corrective steering action is interesting to watch.
