# Intelligent Agents – Unit 3 Reflection

## Agent Architectures

---

## What? (Description)

Unit 3 focused on agent architectures and the different approaches that can be used to design intelligent agents.

The unit developed my understanding of what happens inside an agent. An agent can be viewed as a software program that operates within an architecture, receives information from its environment and selects actions intended to achieve its objectives.

The main agent architecture approaches introduced in this unit were:

- Symbolic reasoning agents
- Reactive agents
- Hybrid agents

The unit also introduced agents with internal state, deductive reasoning, practical reasoning, Belief–Desire–Intention (BDI) agents, subsumption architecture and emergent behaviour.

---

## Symbolic Reasoning Agents

Symbolic reasoning is one of the classical approaches to intelligent-agent design.

A symbolic or deliberative agent maintains an explicit symbolic representation of its environment and uses reasoning to determine which actions should be performed.

In simplified form, this can be represented as:

`Observe → Represent → Reason → Decide → Act`

Symbolic architectures can be useful when an agent needs explicit knowledge, logical reasoning and planning.

However, the lecture introduced two important challenges.

### Transduction Problem

The transduction problem concerns the difficulty of translating a complex real-world environment into an accurate symbolic representation quickly enough for the representation to remain useful.

Real environments may contain changing information, uncertainty, visual information and other complexities that are difficult to capture completely through symbols.

### Symbolic Representation and Reasoning

A second challenge concerns representing and manipulating symbolic information efficiently.

As the amount of knowledge and number of possible actions increase, the reasoning and search processes required to select an action may become computationally expensive.

This helped me understand that an architecture offering sophisticated reasoning may not always be appropriate when an agent needs to respond very quickly to environmental changes.

---

## Deductive Reasoning

The unit also explored deductive reasoning and theorem proving.

The basic principle is that knowledge about the environment and rules regarding appropriate actions can be represented logically.

An agent may then use reasoning to determine which action follows from its current knowledge.

This connects directly with the First-Order Logic material from Unit 2.

Unit 2 introduced formal representations of objects, relationships and rules, while Unit 3 demonstrated how such representations can contribute to agent decision-making.

---

## Agents with State

An agent does not necessarily make decisions based only on its immediate observation.

An agent can maintain an **internal state** containing information about its environment and previous observations.

The basic interaction can be described as:

`Environment → See → Percept → Update State → Select Action → Environment`

The agent observes the environment and generates a percept.

The percept is then used to update the agent's internal state.

The action-selection mechanism uses the updated internal state to determine an appropriate action.

The selected action affects the environment and the cycle repeats.

This is the basis of an **agent control loop**.

An internal state can therefore help an agent make decisions using both current observations and information retained from previous interactions.

---

## Agent Control Loop

A simplified agent control loop consists of the following stages:

1. The agent begins with an initial internal state.
2. The agent observes the environment.
3. The observation generates a percept.
4. The internal state is updated using the new percept.
5. The agent selects an action according to its updated state.
6. The action is performed.
7. The agent observes the environment again.
8. The process repeats.

This continuous cycle demonstrates how intelligent agents can interact dynamically with their environments.

---

## Practical Reasoning

Another important concept introduced in Unit 3 was **practical reasoning**.

Practical reasoning concerns deciding what an agent should do in a particular situation.

The unit distinguished two important stages:

### Deliberation

Deliberation determines **what objective should be achieved**.

The result of deliberation is an intention.

### Means-End Reasoning

Means-end reasoning determines **how the selected objective can be achieved**.

The result is a plan containing actions that can move the agent from its current situation towards its intended goal.

This distinction helped me understand the relationship between objectives, intentions, planning and actions.

---

## Belief–Desire–Intention (BDI) Architecture

The unit introduced the Belief–Desire–Intention model as an important architecture for practical reasoning.

### Beliefs

Beliefs represent information that the agent currently holds about itself, its environment and the state of the world.

### Desires

Desires represent objectives or states that the agent might wish to achieve.

An agent may have multiple desires, and these desires may sometimes compete.

### Intentions

Intentions represent goals to which the agent has committed.

The key distinction between desires and intentions is therefore **commitment**.

A desire is a potential objective.

An intention is an objective that the agent has selected and committed to pursuing.

This distinction is particularly important because an agent may have many possible desires but should select a consistent set of intentions that guide its subsequent actions.

---

## Planning and Block World

The lecture used Block World as an example of planning and symbolic representation.

The environment contains blocks that can be manipulated by a robot arm.

The environment can be represented using predicates such as:

`On(x,y)`

Object x is on top of object y.

`OnTable(x)`

Object x is on the table.

`Clear(x)`

Nothing is on top of object x.

`Holding(x)`

The robot arm is holding object x.

Possible actions include:

- `Stack(x,y)`
- `Pickup(x)`
- `UnStack(x,y)`
- `PutDown(x)`

A goal can be represented as a collection of logical conditions that must become true.

A plan is then a sequence of appropriate actions that transforms the current state into the required goal state.

This example demonstrated the relationship between knowledge representation, goals, actions, preconditions and planning.

---

## Reactive Architectures

Reactive architectures developed partly in response to limitations associated with symbolic reasoning.

Instead of requiring a detailed symbolic model of the environment and extensive reasoning before every action, reactive agents can respond more directly to environmental conditions.

A simplified representation is:

`Perception → Behaviour/Rule → Action`

Reactive architectures can therefore be useful in dynamic environments where rapid responses are important.

However, reduced reliance on explicit symbolic reasoning may also make complex long-term planning more difficult.

---

## Subsumption Architecture

The unit introduced Rodney Brooks' subsumption architecture as an important example of a reactive architecture.

Subsumption architecture organises simple behaviours into layers.

Lower-level behaviours can represent fundamental activities, such as:

- Avoiding obstacles
- Maintaining movement
- Responding to immediate environmental conditions

Higher layers can represent more complex behaviours.

An important advantage of this layered architecture is that individual behaviours can be designed, tested and debugged separately.

Complex overall behaviour can then emerge from interactions between relatively simple behavioural components and the environment.

---

## Emergent Behaviour

Emergent behaviour occurs when the overall behaviour demonstrated by an agent or a collection of agents becomes more complex than the individual rules explicitly programmed into each component.

In other words:

`Simple Rules + Interaction + Environment → Complex Observed Behaviour`

The lecture used examples such as coordinated movement to demonstrate how relatively simple local behaviours can collectively produce more sophisticated patterns.

This concept is important because observed behaviour may not always map directly to one explicitly programmed rule.

Emergence can provide powerful adaptive behaviour but can also introduce challenges when developers need to predict, explain or control the behaviour of a complex agent system.

---

## Hybrid Agent Architectures

Hybrid architectures attempt to combine the strengths of symbolic and reactive approaches.

A hybrid agent can potentially use deliberative reasoning for planning and longer-term objectives while maintaining reactive mechanisms for situations that require an immediate response.

In simplified form:

`Planning and Reasoning + Rapid Reactive Behaviour = Hybrid Architecture`

This approach can be useful in environments where an agent needs both longer-term decision-making and rapid responses to unexpected environmental changes.

The lesson I took from comparing the different approaches is that there is no single architecture that is ideal for every intelligent-agent problem.

Architecture selection should depend on factors such as:

- Complexity of the task
- Required response time
- Environmental uncertainty
- Planning requirements
- Available information
- Computational resources
- Safety and operational risk

---

# Collaborative Discussion 1 – Summary Post

## Summary Post

Over the first three units, my understanding of agent-based systems has developed from viewing agents primarily as autonomous software towards recognising the importance of architecture, reasoning and appropriate control. The growth of agent-based systems has been supported by increasing connectivity, ubiquitous computing, greater artificial intelligence capabilities and the growing delegation of tasks to software. These developments create environments where systems need to react to change while continuing to pursue organisational objectives (Wooldridge, 2009).

My initial post focused particularly on the organisational benefits of agents, including reduced human intervention, distributed decision-making and the ability to respond dynamically to changing conditions. Engaging with my peers' contributions developed this perspective further, particularly around the risks associated with autonomous decision-making. I therefore consider controlled, risk-based autonomy particularly important. Low-risk and reversible decisions may be suitable for autonomous execution, whereas actions with significant operational, financial, security or safety consequences should involve human review. Appropriate controls can include authority limits, activity logging, escalation rules and rollback mechanisms (Parasuraman, Sheridan and Wickens, 2000).

Unit 2 introduced First-Order Logic and demonstrated how formal representations of objects, relationships and rules can support knowledge representation and reasoning. Unit 3 extended this understanding by introducing symbolic, reactive and hybrid agent architectures. Symbolic approaches provide explicit reasoning capabilities, while reactive approaches prioritise rapid responses to environmental changes. Hybrid architectures can combine these strengths, demonstrating that there is no single architecture suitable for every problem (Wooldridge and Jennings, 1995).

The BDI model also clarified the distinction between desires and intentions: desires represent possible objectives, while intentions represent objectives to which an agent has committed. Overall, I now understand that effective agent design requires not simply greater autonomy, but an appropriate combination of reasoning, responsiveness, architecture and human oversight.

---

## So What? (Interpretation)

Unit 3 changed my understanding of intelligent agents because I now recognise that defining an agent's objective is only one part of agent design.

The internal architecture determines how an agent represents information, reasons about its environment, responds to changes and selects actions.

I found the comparison between symbolic and reactive architectures particularly useful.

Symbolic agents can provide explicit reasoning and planning, which may be useful when decisions need to follow structured knowledge or rules. However, this reasoning can introduce complexity and may not always provide sufficiently rapid responses in highly dynamic environments.

Reactive architectures take a different approach by prioritising direct responses to environmental changes. This can support rapid and adaptable behaviour, although complex planning may be more difficult.

Hybrid architectures are therefore particularly interesting because they attempt to combine both capabilities.

This has a practical connection with my professional experience in application programming and automation.

In enterprise automation, some decisions can be based on clearly defined business rules and structured workflows. However, systems must also respond to operational events, exceptions and changing conditions.

An intelligent solution may therefore require different mechanisms for different types of decision.

For example, an enterprise agent could use planning and reasoning to determine how to complete a multi-step service request while maintaining reactive mechanisms for security alerts, system failures or other events requiring immediate escalation.

The BDI model also provided a useful way of thinking about agent decision-making.

The distinction between desires and intentions helped me understand that an agent may identify multiple possible objectives but should commit only to goals that it considers achievable and consistent with its existing commitments.

This is particularly relevant when designing agents that need to prioritise competing business objectives.

---

## What Next? (Action)

Following Unit 3, I want to develop a stronger understanding of how different architectural approaches can be applied to practical intelligent-agent systems.

For future activities, I will consider architecture selection according to the requirements of the problem rather than assuming that one architectural approach is always preferable.

When considering an agent architecture, I will evaluate:

- The type of environment
- The amount of uncertainty
- Required response speed
- Need for long-term planning
- Available knowledge
- Computational complexity
- Consequences of incorrect actions
- Required level of human oversight

For the team design project, I will use the concepts from this unit when considering the proposed architecture for the LLM-powered planning agent.

In particular, I will consider whether the proposed solution requires:

- Deliberative planning
- Reactive behaviour
- Internal state or memory
- Goal management
- Tool interaction
- Human approval
- Exception handling
- A hybrid architecture

I will also continue recording my contribution to team discussions, design decisions and architecture work as evidence for my final e-Portfolio.

---

## Unit 3 Learning Summary

The main concepts I learned in Unit 3 are:

1. An agent architecture defines how the agent's components support perception, reasoning and action.

2. Symbolic agents use explicit representations and reasoning to determine appropriate actions.

3. Symbolic reasoning can face challenges when translating complex real-world environments into useful symbolic representations.

4. Agents can maintain internal state to preserve information from previous perceptions.

5. An agent control loop continuously connects perception, state updates, action selection and environmental interaction.

6. Practical reasoning involves deciding both what should be achieved and how it should be achieved.

7. BDI architectures represent beliefs, desires and intentions.

8. A desire represents a possible objective, while an intention represents an objective to which the agent has committed.

9. Reactive architectures prioritise direct responses to environmental conditions.

10. Subsumption architecture organises simple behaviours into layers.

11. Emergent behaviour can arise from interactions between simple rules, agents and their environment.

12. Hybrid architectures attempt to combine deliberative reasoning with reactive behaviour.

13. Architecture selection should depend on the requirements and characteristics of the problem rather than assuming one architecture is universally superior.

---

## Collaborative Discussion 1 – Completion

The three-stage Collaborative Discussion 1 is now complete:

- [x] Unit 1 – Initial Post
- [x] Unit 2 – Peer Response 1
- [x] Unit 2 – Peer Response 2
- [x] Unit 3 – Summary Post

The discussion developed my understanding of the motivations for agent-based computing, organisational benefits, autonomy, operational risk, human oversight and the importance of selecting appropriate agent architectures.

---

## Unit 3 Evidence

- [x] Unit 3 overview reviewed
- [x] Agent Architecture lecturecast reviewed
- [x] Symbolic reasoning agents studied
- [x] Deductive reasoning reviewed
- [x] Agents with internal state reviewed
- [x] Agent control loop reviewed
- [x] Practical reasoning reviewed
- [x] BDI architecture reviewed
- [x] Difference between desires and intentions understood
- [x] Planning and Block World example reviewed
- [x] Reactive architectures reviewed
- [x] Subsumption architecture reviewed
- [x] Emergent behaviour reviewed
- [x] Hybrid architectures reviewed
- [x] Collaborative Discussion Summary Post completed
- [x] Collaborative Discussion 1 completed
- [x] e-Portfolio link shared
- [ ] Team project evidence to be updated as the project progresses

---

## References

Parasuraman, R., Sheridan, T.B. and Wickens, C.D. (2000) ‘A model for types and levels of human interaction with automation’, *IEEE Transactions on Systems, Man, and Cybernetics – Part A: Systems and Humans*, 30(3), pp. 286–297.

Wooldridge, M.J. (2009) *An Introduction to MultiAgent Systems*. 2nd edn. Chichester: John Wiley & Sons.

Wooldridge, M. and Jennings, N.R. (1995) ‘Intelligent agents: theory and practice’, *The Knowledge Engineering Review*, 10(2), pp. 115–152.
