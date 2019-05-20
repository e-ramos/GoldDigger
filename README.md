# Gold Digger
A Poor Little Pixel Lost in Rectilinear Grid

A Q-Learning Approach


## Files

 - **`GoldDigger.ipynb`** : A Jupyter Notebook that generates the "dungeon" and simulates a "game"
 - **/Output**: contains images that the simulation generates

## Note
The code is best viewed here

https://github.com/e-ramos/GoldDigger/blob/master/GoldDigger.ipynb

## The Task



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

After training, the policy function is refined, such that the pixel can "smell" the gold, and will zero in on it with high probability. Note that there is still a non-zero probability for exploration, my policy improvement approach just merely skews the probability of a high utility action.

In both cases, the pixel wins before it dies of hunger. 
