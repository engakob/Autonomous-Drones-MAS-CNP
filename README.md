# Introduction
The goal of this project is to achieve a collaboration between UAVs to extinguish fire outbreaks in forests and finding a balance between the number of UAV to be deployed and the on-board hardware communication range per UAV using CNP Protocol.


This is a simple Artificial Intelligence project, using Q-Reinforcement Learning to teach a program how to play arcade game snake and eventually reach a super-human level of accuracy and wins.

This code was written from scratch and not built on top or inspired by another project.

The snake learns to play on a NxN grid which can be adjusted in the code, 3x3 being a reasonable environment and 10x10 will take so much time to train.

On a regular i5 - 8GB MAC, a 3x3 snake takes 4-6 hours to start winning, and more than a day to become optimal. This is due to the enormous amount of possible actions that exist for winning or losing. To run on Windows, you might need to add 'r' to the CWD. I will soon update the program to run on MAC and Windows without the need to fix anything before.

According to the Q-Learning algorithm, the program has to scan all possible state-action pairs before deciding the next action, which is based on given rewards. As the program runs, the Q table becomes bigger and bigger which will increase the training time.

The program will generate a 'logs' text-file while training.

I will add a new Python file soon, which will plot the accuracy of the model similar to the graph below. 

### Requirements
Python 2 or 3\
`pip install turtle`\
`pip install tqdm`\
`pip install os`




### How to start
Run Snake_RL.py to start the game and watch the snake learning.
![image text](https://github.com/akob125/AI-Q-Reinforcement-Learning-Snake/blob/master/Media/Plot.jpg)
![image text](https://github.com/akob125/AI-Q-Reinforcement-Learning-Snake/blob/master/Media/GIF.gif)