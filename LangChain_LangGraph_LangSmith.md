
What is LangChain?
- LangChain is a framework for building applications powered by Large Language Models (LLMs).
It provides reusable building blocks and abstractions so you don’t have to reinvent common LLM patterns.
- “Glue together LLMs, tools, data sources, and logic into an application.”

What LangChain gives you?
LangChain is component-oriented:

- LLM wrappers: Connect to OpenAI, Azure OpenAI, Anthropic, etc.
- Prompt templates: Structured, reusable prompts
- Chains: Linear sequences of steps (Prompt → LLM → Output)
- Memory: Conversation history, summaries, buffers
- Retrievers & vector stores: RAG (Retrieval Augmented Generation)
- Tools & Agents: LLMs that can call APIs, databases, code, etc.

What is LangGraph?
- LangGraph is built on top of LangChain and focuses on complex, stateful, and non-linear workflows.
- “Model LLM workflows as graphs instead of chains.”
While LangChain is mostly linear, LangGraph allows:
- Branching
Loops
Conditional decisions
Multi-agent coordination
Persistent state across steps
What makes LangGraph different
LangGraph introduces:

Graph-based execution
Explicit state management
Cycles / retries
Human-in-the-loop steps
Multi-agent systems

Typical LangGraph use cases

Autonomous agents
Multi-step reasoning systems
Approval/review workflows
Planning + execution systems
Long-running AI processes
AI copilots with decision trees
<img width="931" height="505" alt="image" src="https://github.com/user-attachments/assets/789155c3-4619-4eb8-8aa8-e297f40216c0" />

LangGraph does NOT replace LangChain.
Instead:

LangChain = components (LLMs, tools, prompts)
LangGraph = orchestration layer

What is LangSmith?
LangSmith is monitoring tool.

LangGraph
Terminology
Agent workflow are represented as **Graph**
**State** represet the current state of application. State is immutable.
**Node** are python functions that represent agent logic. They receive current **State** as input, do something and return an updated **State**.
**Edges** are python function that determine which **Node** to execute next based on the **State**. They can be conditional of fixed.
**Node** do the work, **Edges** choose what to do next.


