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
