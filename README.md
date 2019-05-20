# Gold Digger
The Poor Little Pixel Lost in a Rectilinear Grid:

A Q-Learning Approach


## Files

 - **`GoldDigger.ipynb`** : A Jupyter Notebook that generates the "dungeon" and simulates a "game"
 - **/Output**: contains images that the simulation generates

## Note
The code is best viewed here

https://github.com/e-ramos/GoldDigger/blob/master/GoldDigger.ipynb

## The Task

I attempted to train a wee little pixel stuck in the square of doom to find its favorite food (Gluten Free RGB[219, 194, 5]).
The pixel has 25 turns before its poor little stomach collapses into a singularity under the intense vacuum of hunger.

As shown in the results, most epochs of memory-less random walks will lead to failure for the poor pixel.
Luckily, in our infinite mercy, we have spawned limitless pixels to torture until a ruleset is perfected so that one lucky pixel will one day survive.

This Q-Learning pixel, has an idea of what it likes:
- Wall = Bad
- Yellow = Yummy!

and can update it's search direction (only a one step memory ala markov) based on this Q function. 

## Results

### Random Walk


| Untrained Random Wandering|
|--|
| ![](https://github.com/e-ramos/GoldDigger/blob/master/Output/Compressed/RandomWalk.gif)|

The Dumb Approach, as we see, our poor little pixel dies of hunger and keeps staying in place. Since the pixel has no memory, when it hits a wall, it doesn't learn and will continue to beat itself against the black walls since it has no internal reward mechanism to break the loop.

### Q-Learning
|Untrained with Q-Policy Improvement|Trained Pixel|
|--|--|
|![](https://github.com/e-ramos/GoldDigger/blob/master/Output/Compressed/QLearning.gif)|![](https://github.com/e-ramos/GoldDigger/blob/master/Output/Compressed/QLearningTrained.gif)|

Defining a Utility Function, we see that even without training, the pixel quickly learns to not beat its head against walls and will only search in locations it has not seen before.

After training, the policy function is refined, such that the pixel can "smell" the gold, and will zero in on it with high probability. Note that there is still a non-zero probability for exploration (even if it means hitting a wall), my policy improvement approach just merely skews the probability of a high utility action.

In both cases, the pixel wins before it dies of hunger. 
