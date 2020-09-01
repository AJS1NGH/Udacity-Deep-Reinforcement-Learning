# Objective
The project uses Deep Q Learning to train an agent to collect yellow bananas and to avoid collecting blue bananas.

Deep Q Learning is a Value based Reinforcement Learning method which uses Neural Networks as a function approximator to approximate the optimal action/state value function for a given environment. As part of the overall model, the Neural Network takes as input states of the environment and uses them to approximate action values for each possible action.

| The [DQN Algorithm](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf) proposed by Mnih et al |
| -----------------------------------|
| ![DQN Algorithm](https://github.com/AJS1NGH/Udacity-Deep-Reinforcement-Learning/blob/master/Project1/images/dqn_algo.jpg) |


# Scores for DQN (Deep Q Networks) Variants

I trained multiple versions of the DQN model to see how proposed improvements in papers impact the training of the agent in this specific environment. The versions implemented are:
* [Basic DQN](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf)
* [Double DQN](https://arxiv.org/abs/1509.06461) - it has been shown that the baseline DQN overestimates action values during training. To counter that, Double DQN uses 2 separate networks - one to pick the next action and another to evaluate that action (choose its action value).
* [Dueling DQN](https://arxiv.org/abs/1511.06581) - Dueling DQN's are based on the fact that for some states of the environment, there isn't much variance in the state-action values - meaning that we don't need to estimate the action-value function (for each action) everytime... only estimating the state-value function should suffice. Therefore Dueling DQN uses 1 backbone model but splits  it into 2 streams - one predicts the state-value and the other advantage-value.
* Dueling Double DQN - combines all of the above

## Results
| Basic DQN | Double DQN |
:-------------------------:|:-------------------------:|
![Basic DQN](https://github.com/AJS1NGH/Udacity-Deep-Reinforcement-Learning/blob/master/Project1/images/DQN.jpg) |  ![Double DQN](https://github.com/AJS1NGH/Udacity-Deep-Reinforcement-Learning/blob/master/Project1/images/Double_DQN.jpg) |

| Dueling DQN | Dueling Double DQN |
:-------------------------:|:-------------------------:|
![Dueling DQN](https://github.com/AJS1NGH/Udacity-Deep-Reinforcement-Learning/blob/master/Project1/images/Dueling_DQN.jpg) |  ![Dueling Double DQN](https://github.com/AJS1NGH/Udacity-Deep-Reinforcement-Learning/blob/master/Project1/images/Dueling_Double_DQN.jpg) |

