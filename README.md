# 🧠 LangGraph Multi-Agent Workflow: Supervisor, Researcher, and Coder

This project demonstrates a multi-agent orchestration system using [LangGraph](https://github.com/langchain-ai/langgraph). It showcases a workflow where a Supervisor Agent dynamically delegates tasks to specialized agents—a **Researcher Agent** and a **Coder Agent**—to collaboratively solve complex problems.

## 🧩 Project Overview

### 🧭 Purpose
To simulate a collaborative AI system where tasks are routed and processed by different agents based on the context and intent of the user query. The architecture is modular, extensible, and built for experimentation with **multi-agent reasoning**.

## 🕹️ Workflow Summary

### 1. **Human Message Initiation**
- The user begins the process by submitting a message or problem (e.g., a request for technical implementation or research clarification).

### 2. **Supervisor Agent (Router)**
- Acts as the decision-maker.
- Receives the user input and decides:
  - Route to **Researcher Agent** (if it's about finding or summarizing information),
  - Route to **Coder Agent** (if it's about writing or improving code),
  - Or terminate if the task is complete.

### 3. **Researcher Agent**
- Gather information or explanations relevant to the user’s question.
- May query a language model with a research-centric prompt.
- Sends the result back to the supervisor or ends the workflow.

### 4. **Coder Agent**
- Implements code based on the user request or prior reasoning by the Researcher.
- Returns output that can be verified or used as input for another cycle.

### 5. **Graph Execution**
- A state machine (`StateGraph`) handles transitions between agents.
- Edges define how the output from one agent determines the next step.
- The system visualizes and executes this graph until the goal is achieved.

# 🧠 LangGraph: Human-in-the-Loop Agent with Tool Usage
This project demonstrates how to build a LangGraph-based AI system that integrates:

- An AI assistant node (LLM)
- A tool node
- Human-in-the-loop decision-making (routing between agent/tool/end)

