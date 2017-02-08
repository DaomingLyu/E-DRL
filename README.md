# E-DRL

## Weely Discussion
1. Experiment Count-based Exploration on pitfall and montezuma's Revenge. [Link](https://github.com/Itsukara/async_deep_reinforce)
2. Improve density models for count-based exploration (PixelCNN, GANs, VAEs, etc)
3. Other exploration strategies [paper](http://www.cs.mcgill.ca/~cs526/roger.pdf) (e.g., Competence Maps, Multiple-Hypothesis Heuristics)
4. Baselines and possible improvements [VIME](https://arxiv.org/abs/1605.09674) [MBIE-EB](https://pdfs.semanticscholar.org/a357/75802eddbcc96001b25a0fbf69895b994219.pdf)
5. Novel ideas to incorporate exploration into network structure


Exploration Strategies for Deep Reinforcement Learning

We plan to explore the exploration strategies for DRL to overcome sparse reward games such as MONTEZUMA's REVENGE and PITFALL.
PITFALL is actually unsolved and all current models resulting in pessimistic behaviors (e.g., jumping around the starting point)

We'll first run baselines of Dueling DQN and A3C on Montezuma's Revenge and PITFALL. Here are the baselines:

We'll implemented counter-based approach on both tasks.

We'll try my approach on that.

Some ideas:

1. Do we really need time discount on reward since the reward are generally all long-term?

2. Since it gets a lot of negative rewards before it is possible to get to a positive reward, current models tend to punish these policies: which means it would not go any direction, and just stay at the starting point. How to overcome this? Is it good to clip or reduce the negative reward? Or how to improve the possibility of coming to a positive reward point? Or how to strengthen the experience when getting a positive reward?

3. Based on count-based methods, what we actually need is a density estimator for an unseen image. Could we use Variational Autoencoder, Generative Adversarial Nets, Bolzman Machines or any other approaches to build the estimator?

4. Is it possible to directly embed the exploration strategy into DQN training?
