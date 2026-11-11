# Intelligent Agents – Unit 1 Reflection

## Introduction to Agent-Based Computing

---

## What? (Description)

Unit 1 introduced me to the foundations of agent-based computing and the technological developments that have contributed to the growth of intelligent agents.

The lecturecast identified five important trends in computing:

- **Ubiquity** – computing technologies are increasingly embedded in everyday devices and environments.
- **Interconnection** – modern computing systems are increasingly connected through networks and distributed infrastructures.
- **Intelligence** – computers are capable of performing increasingly complex tasks.
- **Delegation** – people increasingly delegate tasks and decision-making responsibilities to computer systems.
- **Human orientation** – interaction with technology has progressively moved towards concepts and interfaces that are more natural for humans.

Together, these trends create a need for systems that can operate with a greater degree of independence and respond effectively to complex and changing environments.

The required reading introduced an agent as a computer system situated within an environment and capable of autonomous action in that environment in order to achieve its design objectives (Wooldridge, 2009).

I learned that an intelligent agent can demonstrate several important characteristics:

- **Autonomy** – operating without continuous human intervention.
- **Reactivity** – perceiving and responding to environmental changes.
- **Proactiveness** – taking initiative and pursuing objectives.
- **Social ability** – interacting with other agents or humans to achieve objectives.

The unit also introduced the relationship between an agent and its environment. An agent receives information about its environment through sensors or software-based perception mechanisms and influences the environment through actions.

Importantly, an agent normally has only partial control over its environment. Performing the same action in apparently similar circumstances may therefore produce different results. This means that intelligent agents must be designed to handle uncertainty and possible failure.

The reading also introduced different environmental characteristics, including:

- Accessible and inaccessible environments
- Deterministic and non-deterministic environments
- Static and dynamic environments
- Discrete and continuous environments

Another important concept was that actions can have **preconditions**. An agent may have the capability to perform a particular action, but the action should only be performed when the appropriate conditions are satisfied.

I also learned about examples of agent-like systems, including:

- Control systems such as thermostats
- Software daemons
- Reactive systems
- Autonomous control systems

A key point from the unit was the distinction between reactive and proactive behaviour. An intelligent agent should be capable of reacting to environmental changes while continuing to pursue its objectives.

---

## Collaborative Discussion 1 – Agent-Based Systems

### Initial Post

The rise of agent-based systems has been influenced by major developments in computing, including increased connectivity, ubiquitous computing, greater system intelligence and the growing delegation of tasks to software. Wooldridge describes an agent as a computer system situated within an environment that can act autonomously to achieve its design objectives (Wooldridge, 2009). Intelligent agents also demonstrate reactivity, proactiveness and social ability, enabling them to respond to environmental changes, pursue goals and interact with other agents.

For organisations, these capabilities can provide important benefits. Agent-based systems can reduce the need for continuous human intervention, respond to changing conditions and support distributed decision-making. They are particularly valuable in complex environments where data, systems and responsibilities are distributed. Unlike conventional software that follows predetermined instructions, agents can select appropriate actions according to their objectives and their understanding of the environment (Wooldridge, 2009).

Modern LLM-powered agents extend these ideas by combining language models with reasoning, planning and external tool interaction. For example, ReAct combines reasoning with actions, enabling language models to interact with external environments while completing tasks (Yao et al., 2023). LLM-based autonomous agents can also incorporate capabilities such as planning, memory and tool use (Wang et al., 2024).

However, greater autonomy introduces challenges around reliability, incorrect decisions and governance. Therefore, for my own agent design, I would use **controlled autonomy**, allowing the agent to complete approved low-risk tasks independently while escalating uncertain or high-impact decisions for human review.

---

## Additional Research – LLM-Powered Agents

As part of Unit 1, I explored how LLM-powered agents can support activities such as research, information gathering and task completion.

Modern LLM-powered agents extend traditional agent concepts by combining large language models with capabilities such as:

- Reasoning
- Planning
- Task decomposition
- Memory
- Tool use
- Interaction with external information sources
- Evaluation of intermediate results

The ReAct approach combines reasoning and acting, allowing a language model to reason about a task while also interacting with external environments or tools (Yao et al., 2023).

Research on LLM-based autonomous agents also suggests that planning, memory, action and tool interaction can form important components of agent architectures (Wang et al., 2024).

### Design Decision

For my own agent design, I would implement **controlled autonomy with human oversight**.

The agent could independently perform approved and low-risk activities, such as gathering information, organising information or carrying out predetermined actions.

However, if the agent encounters uncertainty, sensitive information, an unexpected situation or a decision with significant impact, the task should be escalated for human review.

This design approach would allow the system to benefit from agent autonomy while maintaining appropriate governance and control.

---

## So what? (Interpretation)

Unit 1 helped me develop a clearer understanding of the difference between conventional automation and intelligent agent-based systems.

This distinction is particularly relevant to my professional experience in application programming, RPA and enterprise automation.

Traditional automation generally follows predefined workflows and business rules. For example, an RPA process may execute a predetermined sequence of activities when particular conditions are satisfied. The automation is effective when the process and possible exceptions are clearly defined.

An intelligent agent introduces a different approach. Instead of specifying every individual step, the system may be given an objective and allowed to determine which permitted actions are appropriate according to its current environment.

This helped me understand why autonomy is central to agent-based computing.

However, I also learned that autonomy should not automatically mean complete independence.

An important concept from the unit was the need to balance **reactivity and proactiveness**. An agent that focuses only on its original plan may fail to respond appropriately when circumstances change. On the other hand, an agent that continuously reacts to every environmental change may fail to remain focused long enough to achieve its objectives.

This demonstrates that effective intelligent-agent design requires an appropriate balance between pursuing goals and responding to environmental changes.

The concept of uncertainty was also important. Because agents generally have only partial control over their environments, an action does not necessarily guarantee its intended outcome. The agent therefore needs mechanisms for detecting changes, recognising failures and determining whether its current course of action remains appropriate.

The unit also helped me connect classical intelligent-agent theory with modern LLM-powered agents. Although current LLM agents use technologies that were not available when earlier agent theories were developed, concepts such as autonomy, environment, goals, actions, planning and interaction remain highly relevant.

From an organisational perspective, I can see significant potential for intelligent agents in areas such as automation, service management, information gathering and operational support. However, organisations also need to consider reliability, security, accountability, governance and human oversight when increasing the autonomy given to these systems.

For this reason, I consider **controlled autonomy** particularly relevant to enterprise environments. Routine and low-risk decisions could potentially be automated, while uncertain, sensitive or high-impact decisions remain subject to human review.

---

## What next? (Action)

In the next units, I want to develop a deeper understanding of how intelligent agents actually make decisions and how different agent architectures influence their behaviour.

In particular, I want to explore:

- Different intelligent agent architectures
- Planning and decision-making
- Reactive and proactive agents
- Multi-agent interaction
- Agent communication
- Cooperation and coordination
- LLM-powered agent architectures
- Memory and tool use
- Human-agent interaction
- Ethical and governance considerations

For practical activities, I will maintain my work in GitHub and document relevant coding exercises and agent experiments as part of this e-portfolio.

I also intend to connect the theoretical concepts in the module with my professional experience in automation and application development. In particular, I want to examine where intelligent agents may provide additional capabilities beyond traditional rule-based automation and RPA.

For future agent designs, I will consider the level of autonomy appropriate to the task rather than automatically aiming for maximum autonomy. I will also consider mechanisms for human review, exception handling and escalation where agent decisions involve uncertainty or higher levels of risk.

---

## Unit 1 Learning Summary

The main concepts I learned in Unit 1 are:

1. Agent-based computing has grown alongside trends in ubiquity, interconnection, intelligence, delegation and human-oriented computing.
2. An agent operates within an environment and performs actions to achieve defined objectives.
3. Autonomy is a central characteristic of agency.
4. Intelligent agents should demonstrate an appropriate combination of reactivity and proactiveness.
5. Social ability enables agents to interact with humans and other agents.
6. Agents normally have only partial control over their environments.
7. Actions may have preconditions that determine when they can appropriately be performed.
8. Dynamic and uncertain environments make agent decision-making more challenging.
9. Modern LLM-powered agents extend classical agent concepts through reasoning, planning, memory and tool interaction.
10. Organisational use of intelligent agents requires consideration of reliability, governance and human oversight.

---

## Unit 1 Evidence

- [x] Module introduction reviewed
- [x] Unit 1 lecturecast completed
- [x] Core reading reviewed
- [x] Wooldridge Chapter 2 reviewed
- [x] Collaborative Discussion 1 Initial Post completed
- [x] Minimum 200-word requirement met
- [x] In-text citations included
- [x] Minimum three references included
- [x] LLM-powered agent research completed
- [x] Agent design decision identified
- [x] Unit 1 reflection completed
- [ ] Peer Response 1 – to be completed in Unit 2
- [ ] Peer Response 2 – to be completed in Unit 2
- [ ] Summary Post – to be completed in Unit 3

---

## References

Wooldridge, M.J. (2009) *An Introduction to MultiAgent Systems*. 2nd edn. Chichester: John Wiley & Sons.

Yao, S. et al. (2023) ‘ReAct: Synergizing reasoning and acting in language models’, *International Conference on Learning Representations (ICLR)*.

Wang, L. et al. (2024) ‘A survey on large language model based autonomous agents’, *Frontiers of Computer Science*, 18, 186345.
