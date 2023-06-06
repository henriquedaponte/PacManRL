# PacManRL
Writing a PacMan RL agent based on QLearning algorithm


v1 (05/24/2023)

in valueIterationAgents.py wrote:

def runValueIteration(self)

def computeQValueFromValues(self, state, action)

def computeActionFromValues(self, state)


v2 (05/30/2023)

in analysis.py

change the noise in question2() to 0.01 so that the agent would cross the bridge in getBridgeGrid() (gridworld.py)


v3(05/30/2023)

in analysis.py:

Modified discount, noise, and living reward parameters so the agent (optimal policy) would achieve desired behavior in getDiscountGrid()

def question3a(): Agent would prefer the close exit (+1), risking the cliff (-10)
 
def question3b(): Agent would prefer the close exit (+1), but avoiding the cliff (-10)

def question3c(): Agent would prefer the distant exit (+10), risking the cliff (-10)

def question3d(): Agent would prefer the distant exit (+10), avoiding the cliff (-10)

def question3e(): Agent would avoid both exits and the cliff (so an episode should never terminate)


v4 (05/31/2023)

in qlearningAgents.py:

Wrote the following methods of the class QLearningAgent:

def __init__(self, **args):
        "You can initialize Q-values here..."
    

def getQValue(self, state, action):
        """
          Returns Q(state,action)
          Should return 0.0 if we have never seen a state
          or the Q node value otherwise
        """
        
def computeValueFromQValues(self, state):
        """
          Returns max_action Q(state,action)
          where the max is over legal actions.  Note that if
          there are no legal actions, which is the case at the
          terminal state, you should return a value of 0.0.
        """
        
  def computeActionFromQValues(self, state):
       """
         Compute the best action to take in a state.  Note that if there
         are no legal actions, which is the case at the terminal state,
         you should return None.
       """
       
 def update(self, state, action, nextState, reward):
        """
          The parent class calls this to observe a
          state = action => nextState and reward transition.
          You should do your Q-Value update here
        """


v5 (05/31/2023):

in qlearningAgents.py:

implemented getAction() method to follow epsilon-greedy

# FINAL VERSION (06/05/2023)

in qlearningAgents.py

Improved the Q-Learning agent to use linear function approximation (reduced the number of required training episodes by a factor of 5 approximately) by implementing the following class

class ApproximateQAgent(PacmanQAgent)
