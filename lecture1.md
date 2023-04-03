# Lecture 1

## What is AI?
- A field of computer science concerned with understanding and building intelligent agents that can:
  - perceive
  - understand
  - predict
  - manipulate
  - learn
- this is very hard, yet possible, quite useful and a lot of fun!
- Monolithic approach unnecessary for usefulness
- General intelligence versus task-specific intelligence; operating in a controlled environment versus in the wild
- Broad goals of AI are shared with other disciplines, including philosophy, cognitive science (psychology) and neuroscience. Some key distinctions:
  - understand versus build
  - Rational versus human-like
- Specific goals of AI are shared with other disciplines, including linguistics (perception), statistics (learning), and mathematical logic (knowledge and reasoning)

## The Turing Test
- Proposed by Alan Turing in 1950 as an operational test of intelligence: fool a human interrogator into believing the agent is a human. To pass the test, one needs:
  - natural language processing
  - knowledge representation
  - automated reasoning
  - machine learning
- Avoided physical interaction between interrogator and agent, excluding need for:
  - Computer Vision
  - Robotics
- Robot-like vs human-like

## Knowledge Representation
- How do we represent knowledge?
  - factual knowledge (facts)
  - uncertain knowledge (beliefs)
- What knowledge is relevant?
- How do we aquire knowledge?
  - experts

## KR: How do we represent knowledge?
- Propositional logic
- first order logic
- beliefs:
  - representations: belief networks (Bayesian networks), fuzzy logic

## Reasoning
- How can we formalize the reasoning process?
  - deduction: what is implied by what we know?
  - belief revision: What beliefs to give up in case of a contradiction?
  - Causality: What is the cause of an event?
- How can we reason efficiently?
  - time
  - space (memory)
  - footprint

## Applications of KR&R (Knowledge Representation and reasoning)
- Medical diagnosis
- Theorem proving (Mathematics)
- Formal verification
- Cognitive tasks: planning, explanation, etc
- Product configuration

## Natural Language Processing (NLP)
- Understand natural language:
  - list all employees that have been working here for more than two years and have not gotten a raise since then.
- Generate natural language:
  - there are actually only two such employees, do you just need their names?
- Text summarization:
  - here's a 100 word abstract of the article
- Machine translation
  - Convert text from one language into another

## Natural Language Processing (vs Understanding)
- Why is it hard? Context, ambiguity, commonsense.
  - Syntactic ambiguity
  - semantic ambiguity
  - pragmatic ambiguity
- Two key approaches:
  - classical (understanding): Provide the system with rich knowledge of the world, perform thorough syntactic, semantic and pragmatic analysis, disambiguate using knowledge and reasoning
- Modern (Processing): Reply on data and use machine learning

## Machine Learning
- Using experiences and observations to improve future performance (actions):
  - What aspects of performance to be improved?
  - How to represent the output of a learning process?
  - What feedback is available? (type of data/input)
- Supervised: Situations and actions they should lead to
- Unsupervised: Situations only, find patterns
- Reinforcement: Give positive/negative feedback on sequences of actions

## Supervised Learning
- character recognition
- image segmentation
- image analysis

## Unsupervised Learning
- Recommender systems

## Reinforcement Learning
- playing games

## Robotics
- Robots: Physical agents that perform tasks by manupulating the world
- Equipped with:
  - effectors
  - sensors
- Common categories of robots:
  - manipulators
  - mobile robots
  - mobile robots (humanoid) 