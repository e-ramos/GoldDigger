# Gold Digger
A Poor Little Pixel Lost in Rectilinear Grid

A Q-Learning Approach


## Files

 - **`GoldDigger.ipynb`** : A Jupyter Notebook that generates the "dungeon" and simulates a "game"
 - **/Output**: contains images that the simulation generates

## Note
The code is best viewed here

https://github.com/e-ramos/GoldDigger/blob/master/GoldDigger.ipynb

## The task



## Results

### Random Walk

The Dumb Approach, as we see, our poor little pixel dies of hunger and keeps staying in place. Since the pixel has no memory, when it hits a wall, it doesn't learn and will continue to hit it since it has no internal reward mechanism to break the loop.


| Untrained Random Wandering|
|--|
| ![](https://github.com/e-ramos/GoldDigger/blob/master/Output/Compressed/RandomWalk.gif)|



|Untrained with Q-Policy Improvement|Trained Pixel|
|--|--|
|![](https://github.com/e-ramos/GoldDigger/blob/master/Output/Compressed/QLearning.gif)|![](https://github.com/e-ramos/GoldDigger/blob/master/Output/Compressed/QLearningTrained.gif)|
