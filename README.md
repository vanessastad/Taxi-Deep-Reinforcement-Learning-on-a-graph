# Deep-Reinforcement-Learning to train a Taxi on a graph


Description:
We build a graph with a prefixed number of nodes (in our case 8). Our Didi (it's like an Uber) has to pick up and to drop off a passenger in specified nodes. All the nodes correspod to possible passenger locations and destinations. The Didi pays -1 for every allowed step, -100 if the action is forbidden (for example to pick up or to drop off the passenger in a wrong node), -100 for impossible transitions and it receives a positive reward (+1000) and the event ends only if it drops off the passenger in the correct node. The training of the Didi is based on sixty-four different conditions.
Observations The number of states (576) is a combination of the num_nodes (8), the num_pass_idx (9) and the num_dest_idx (8). The num_pass_idx is 9 because there are 8 possible locations to pick up the passenger and the ninth case represents the possibility that the passenger is inside the Didi.

Action:
The number of actions is equal to num_nodes + 2. Notably the actions are to pick up, to drop off and all the possible transitions towards a particular node.

In this specific example:

action 0 means to go to the 0 node

action 1 means to go to the 1 node

...

action 7 means to go to the 7 node

action 8 means to pick up

action 9 means to dropp off



Render:

yellow: passenger position

blue: destination

green: empty Didi

red: full Didi

orange: pick up or drop off in wrong nodes


Rewards:
The reward depends on the action

-1 for each allowed action

-100 if drop off or pick up are executed in wrong nodes

-100 if the transition is impossible because there is not edge

+1000 if the Didi drops off the passengerse in the correct dest_node




It's possible to change the number of nodes. My colleagues and I worked on different problems and we arrived to solve one with 20 nodes.
This project was firtly developed with Google Coolab that was very useful because I worked on it with two colleagues. You can run it on Jupyter too with few modifications. A more complex problem was solved with Deep Reinforcement Learning, check out my repositories for more informations. Google Colab: upload gym-Didi as a zip file in the session storage of Google colab. Jupyer: cancel "!unzip gym-Didi-NN8.zip" and use just "!pip install -e /your_path/gym-Didi-NN8". Cancel "import seaborn.apionly as sns" and the "aani = matplotlib.animation.FuncAnimation(fig, update, frames = len(frames), interval = 500, repeat = True)
ani" at the end of the main.
If you need any information, contact us:

vanessa.staderini@gmail.com

95vittoriar@gmail.com

tommaso3d@gmail.com

