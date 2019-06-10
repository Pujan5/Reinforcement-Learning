# Reinforcement-Learning
We're going to be working with OpenAI's gym, specifically with the "MountainCar-v0" environment. To get gym, just do a pip install gym.

For the various environments, we can query them for how many actions/moves are possible. In this case, there are "3" actions we can pass. This means, when we step the environment, we can pass a 0, 1, or 2 as our "action" for each step. Each time we do this, the environment will return to us the new state, a reward, whether or not the environment is done/complete, and then any extra info that some envs might have.


new_q = (1 - LEARNING_RATE) * current_q + LEARNING_RATE * (reward + DISCOUNT * max_future_q)
DISCOUNT

and
max_future_q

The DISCOUNT is a measure of how much we want to care about FUTURE reward rather than immediate reward. Typically, this value will be fairly high, and is between 0 and 1. We want it high because the purpose of Q Learning is indeed to learn a chain of events that ends with a positive outcome, so it's only natural that we put greater importance on long terms gains rather than short term ones.

The max_future_q is grabbed after we've performed our action already, and then we update our previous values based partially on the next-step's best Q value. Over time, once we've reached the objective once, this "reward" value gets slowly back-propagated, one step at a time, per episode.

The LEARNING_RATE is between 0 and 1, same for discount. The EPISODES is how many iterations of the game we'd like to run.

