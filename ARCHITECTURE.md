Overview

This project demonstrates a multi-agent workflow using Hermes Agent (brain) and OpenClaw (hands).

Hermes Agent = Orchestrator
OpenClaw = Coding Agent
Slack = Communication Layer
Groq (Kimi K2) = Language Model Provider
Agent Responsibilities
Hermes Agent (Brain)

Responsibilities:

Understand user requests
Create execution plans
Break tasks into smaller steps
Store and recall memory
Trigger skills automatically
Assign coding work to OpenClaw
Report progress
OpenClaw (Hands)

Responsibilities:

Receive coding tasks
Generate code
Execute code
Report results
Handle revisions and follow-up changes
Communication Flow

Human
↓
Hermes Agent
↓
Slack (#sprint-main)
↓
OpenClaw
↓
Slack (#agent-coder)
↓
Hermes Agent
↓
Human Review

Slack Channels
#sprint-main

Primary coordination channel.

#agent-orchestrator

Hermes planning and orchestration logs.

#agent-coder

OpenClaw coding progress and outputs.

#ci-cd

Automated validation and test reports.

#human-review

Human approval and intervention decisions.

Model Routing
Planning

Model:
Kimi K2 (Groq)

Used for:

Planning
Task decomposition
Memory operations
Coding

Model:
Kimi K2 (Groq)

Used for:

Code generation
Code revisions
Error fixing
Validation

Human approval gate before final output.

Human-in-the-Loop

The system requires human approval before final completion.

Workflow:

Hermes creates a plan.
OpenClaw executes tasks.
Results are reported.
Human reviews output.
Final approval is given.
