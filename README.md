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

# Agent would prefer the close exit (+1), risking the cliff (-10)
def question3a():
    answerDiscount = 0.2
    answerNoise = 0
    answerLivingReward = -0.6
    return answerDiscount, answerNoise, answerLivingReward
    # If not possible, return 'NOT POSSIBLE'
    
# Agent would prefer the close exit (+1), but avoiding the cliff (-10)
def question3b():
    answerDiscount = 0.5
    answerNoise = 0.4
    answerLivingReward = -1
    return answerDiscount, answerNoise, answerLivingReward
    # If not possible, return 'NOT POSSIBLE'
    
# Agent would prefer the distant exit (+10), risking the cliff (-10)
def question3c():
    answerDiscount = 0.7
    answerNoise = 0.1
    answerLivingReward = 0
    return answerDiscount, answerNoise, answerLivingReward
    # If not possible, return 'NOT POSSIBLE'

# Agent would prefer the distant exit (+10), avoiding the cliff (-10)
def question3d():
    answerDiscount = 0.9
    answerNoise = 0.5
    answerLivingReward = 0
    return answerDiscount, answerNoise, answerLivingReward
    # If not possible, return 'NOT POSSIBLE'

# Agent would avoid both exits and the cliff (so an episode should never terminate)
def question3e():
    answerDiscount = 0.2
    answerNoise = 0.8
    answerLivingReward = 0
    return answerDiscount, answerNoise, answerLivingReward
    # If not possible, return 'NOT POSSIBLE'
