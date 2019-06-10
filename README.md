# Reinforcement-Learning
We're going to be working with OpenAI's gym, specifically with the "MountainCar-v0" environment. To get gym, just do a pip install gym.

For the various environments, we can query them for how many actions/moves are possible. In this case, there are "3" actions we can pass. This means, when we step the environment, we can pass a 0, 1, or 2 as our "action" for each step. Each time we do this, the environment will return to us the new state, a reward, whether or not the environment is done/complete, and then any extra info that some envs might have.
