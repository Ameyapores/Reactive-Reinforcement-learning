# Reactive-Reinforcement-learning

A framework to generate reactive behaviours, motivated from Subsumption architecture from 1980s. In our archihtecture each  behaviour is represented as a separate module (Deep network), having direct access to processed sensory information. Each module has an individual specific goal. We use a trivial form of imitation learning, called Behaviour cloning, to train these distinct behaviour layers.

<img align="center" src="images/ameya.png" width="1500"> 

The primary goal of picking the object is subdivided into simpler subtasks. For each subtask, there are reactive networks which are trained specially for movement in x, y and z. First, the state vector (in the form of coordinates of objects) is given as an input to the Feature extraction layer. The extracted features are relayed on to the reactive layers deciding the movement of the end-effector. To simplify terminology, we use the following corresponding letters for denoting the subordinate actions: Approach (a), manipulate (b) and retract (c).


## Implementation details

Here, we use the OpenAI simulator FetchPickandPlace which provides kinematic state vector as an input to our network.
For installing OpenAI fetch simulator: Refer to [Fetch](https://openai.com/blog/ingredients-for-robotics-research/)

### Step 1: Train on approach
## Results
<img src="images/fetch_rotate.gif" width="600"> 

Comparison of end-to-end learning vs proposed reactive Reinforcement architecture.

<img src="images/Figure_4.png"> 
