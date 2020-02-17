# AI-MDP-and-Reinforcement-Learning
## Problem Description
You would like to drink coffee. However, the coffee machine is in a different room and you do not want to go and get it yourself. 
So, you would like to build a robot and train it to get you coffee. 
The floor, unfortunately, is slippery, and so the robot may spill the coffee while going from the coffee machine to you. 

You goal: build a robot that can plan its path intelligently so as to maximize the expected utility of drinking coffee. Note that while drinking hot coffee is worth 100 points to you, every step the robot moves cools down the coffee, effectively reducing the number of points by half. So, if the robot performs two steps from the coffee machine and gives you the coffee, you get 25 points. 

Some details:
1.	The reward for drinking a hot cup of coffee is 100. The reduced reward due to the time spent by the robot getting you the coffee is handled by a discount factor of 0.5. 
2.	The probability of spilling the coffee depends on the specific location. For example, the probability of spilling the coffee at location (1,1) may be 0.5 while the probability of spilling the coffee at location (2,1) may be 0.25. 

♦ Markov Decision Process and Value Iteration: BelmanUpdate Class & ValueIteration Class.

  --> Belman Update by: V(state) <- Reward(state,action)+ §*Sigma[Pr(s|state,action)*V(s)], where § is the discount factor.

♦ Reinforcement Learning with Q-Learning: EpsilonGreedyAgent & QValueUpdate.

  --> QValueUpdate: Q(state,action) <- (1-¶)*Q(state,action) + ¶*(reward + §*Max-of-all-b-Belongs-to-actions{Q(newState,b)}), where ¶ is the learning rate and § is the discount factor.

## Usage
1. To check your implementation, you can run the Runner class and observe the average discounted reward you get by running your agent on a randomly generated problem, and on a pre-generated problem. 
These will be shown in the lines starting with "MDP:" 
The expected average for the pre-generated problem is 31.64.

2. To check your implementation, you can run the Runner class and observe the average discounted reward you get by running your agent on a randomly generated problem. 
These will be shown in the lines starting with "RL:". 
If implemented correctly, you should expect to see the average utility rise and converge through many iterations.

## Credits
Developed and solved by Daniel Ben Simon & Eran toutian.
Students 4th year, Information and Software Systems Engineering, Ben Gurion University of The Negev, Israel.
