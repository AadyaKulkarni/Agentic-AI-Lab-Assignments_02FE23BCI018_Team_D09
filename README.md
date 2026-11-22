Agentic AI Systems — All 14 Labs & Assignments

A collection of Python-based weekly parallel assignments exploring the design, implementation, evaluation, and governance of AI agents. The work is organized into 14 lab folders, with each lab focusing on a different agentic concept and its practical application.

The assignments use small, inspectable demonstrations—such as a study planner, campus data assistant, research agent, cloud operations agent, and campus help-desk agent—to illustrate how agent systems plan tasks, use tools, retain context, coordinate workflows, and apply safety checks.
Project reference: CareerPilot – Placement Readiness & Career Intelligence Portal is the related project repository provided as context. CareerPilot is a separate full-stack placement-readiness application; this repository documents the weekly Python lab assignments in the uploaded archive.

Table of Contents
- Learning Objectives
- Weekly Lab Overview
- Repository Structure
- Technologies and Concepts
- Getting Started
- Running the Assignments
- Implementation Notes
- Future Scope
Learning Objectives
Across the 14 labs, the assignments explore how to:
- Build agents around goals, plans, actions, observations, and revisions.
- Select and invoke tools through structured interfaces.
- Package repeatable behavior as reusable skills.
- Separate short-term context from longer-term memory and retrieve relevant information.
- Expose capabilities through a discoverable, MCP-style interface.
- Build extensible agent runtimes and node-based workflows.
- Coordinate multiple agents concurrently and resolve conflicting outputs.
- Conduct evidence-based research with source tracking and quality assessment.
- Diagnose operational incidents and keep higher-risk actions under human approval.
- Apply an agentic software-development lifecycle with independent testing.
- Add safety controls, evaluation gates, audit trails, and domain-specific reasoning.
- Integrate tools, skills, memory, workflow orchestration, evaluation, and safety in a capstone system.
Weekly Lab Overview
Lab	Topic	Main implementation / focus
01	Agent vs. Chatbot	A study-planner agent that follows a Goal → Plan → Act → Observe → Revise loop, reads an existing schedule, and adapts its plan to feedback.
02	Tool-Using Agent	A campus data assistant that selects from structured tools such as a calculator, CSV reader, and mock events API; includes a notification capability that drafts rather than sends a message.
03	Skill Creation	A reusable research-summary skill with defined instructions, workflow, constraints, and examples; tested against multiple inputs and low-evidence or multi-claim sources.
04	Memory and Retrieval	A multi-session project assistant with topic-scoped retrieval, source-tagged answers, conflict detection, and memory staleness/retention handling.
05	MCP-Style Connector	A mini integration server that publishes discoverable resources and tools, including file listing/reading, SQLite queries, and a mock API, with permission boundaries.
06	Agent Runtime	A mini personal-agent runtime combining an interface, runtime loop, skill registry, tools, scoped memory, audit logging, per-user rate limits, and failure escalation.
07	Agentic Node Graph	A campus-event workflow represented as connected nodes with declared inputs, outputs, ownership, success criteria, failure paths, security scanning, and retry/escalation behavior.
08	Parallel Agent Swarm	Multiple role-specific agents work concurrently on a hackathon-planning task; their outputs are merged, critiqued, and reconciled.
09	Deep Research Agent	A research pipeline that searches, extracts, compares, and synthesizes evidence while linking conclusions to source records and weighing source quality.
10	Cloud Operations Agent	An incident-diagnosis workflow that observes logs, reasons about deployment or database issues, proposes remediation, and restricts automatic execution to low-risk actions.
11	Agentic SDLC Factory	A feature-development pipeline covering requirements, design, code, independent tests, review, documentation, and release, with human checkpoints and regression testing.
12	Safety, Evaluation, and Governance	A production-change agent with controls such as permission limits, cost checks, evaluation requirements, audit logging, and mandatory re-evaluation.
13	Discipline-Specific Engineering Agent	Agentic patterns applied to engineering data, including electrical-load forecasting and mechanical predictive-maintenance scenarios using simulated readings and thresholds.
14	Capstone Project Studio	An integrated campus help-desk agent combining a node graph, multiple tools, reusable skills, memory, prompt/execution logs, evaluation, and safety controls.


Each lab folder contains the corresponding assignment scripts. Some labs also include a named demonstration script that brings the week's main concept together.
Repository Structure
The uploaded archive is organized as follows:
02FE23BCI007/
└── lab-assignments/
    ├── lab-01/
    ├── lab-02/
    ├── lab-03/
    ├── lab-04/
    ├── lab-05/
    ├── lab-06/
    ├── lab-07/
    ├── lab-08/
    ├── lab-09/
    ├── lab-10/
    ├── lab-11/
    ├── lab-12/
    ├── lab-13/
    └── lab-14/
The folders contain assignment-1.py and assignment-2.py files, along with additional topic-specific scripts where applicable. Examples include:
- study_planner.py – Lab 1 study-planner agent
- campus_data_assistant.py – Lab 2 tool-using assistant
- research_summary.py – Lab 3 reusable research skill
- project_assistant.py – Lab 4 memory and retrieval assistant
- mcp_server.py – Lab 5 MCP-style integration server
- agent_runtime.py – Lab 6 mini agent runtime
- Node Graph.py – Lab 7 node-graph workflow
- Parallel Swarm.py – Lab 8 parallel multi-agent workflow
- Deep Research Agent.py – Lab 9 research workflow
- cloud_operations.py – Lab 10 cloud operations agent
- SDLC Factory.py – Lab 11 agentic SDLC workflow
- SEG.py – Lab 12 safety, evaluation, and governance
- predictive_maintenance.py – Lab 13 engineering-agent example
- campus_helpdesk.py – Lab 14 integrated capstone
Technologies and Concepts
Primary language: Python 3

The scripts demonstrate Python concepts and agent-system patterns including:
- Classes, functions, and data structures
- Structured tool inputs and outputs
- CSV processing and SQLite
- File and path handling
- Dataclasses and date/time handling
- Concurrent execution with concurrent.futures
- Workflow orchestration and node graphs
- Memory records, retrieval, and audit logs
- Rule-based evaluation, validation, and safety checks
The assignments are primarily self-contained demonstrations and use simulated data or mock services in several places. The presence of an agent workflow does not necessarily mean that it calls a live LLM or an external service.
Getting Started
Prerequisites
- Python 3.10 or later recommended
- A code editor such as Visual Studio Code
- A terminal or command prompt
Most scripts use Python's standard library. No project-wide third-party dependency installation is specified by the supplied assignment files.
Setup
1. Download or clone this repository.
2. Open the project folder in your editor.
3. Open a terminal in the relevant lab folder.
4. Run the Python script for the assignment you want to explore.
Example:
cd 02FE23BCI007/lab-assignments/lab-01
python study_planner.py
If you are running an assignment script instead, use its filename, for example:
python assignment-1.py
On systems where the Python 3 command is python3, replace python with python3.
Running the Assignments
Run each script independently from its lab directory. For example:
# Lab 2
cd 02FE23BCI007/lab-assignments/lab-02
python campus_data_assistant.py

# Lab 6
cd 02FE23BCI007/lab-assignments/lab-06
python agent_runtime.py

# Lab 8
cd "02FE23BCI007/lab-assignments/lab-08"
python "Parallel Swarm.py"

# Lab 14
cd "02FE23BCI007/lab-assignments/lab-14"
python campus_helpdesk.py
Some scripts contain predefined sample inputs and simulated scenarios. Review the relevant file before execution to understand its test cases and expected behavior.
Implementation Notes
- Demonstration scope: Several integrations are mocked or represented with local sample data. For example, the campus assistant uses a mock events API and in-memory data stores.
- No implied production deployment: These lab implementations demonstrate concepts and are not, by themselves, production-ready services.
- Safety and permissions: The later labs explicitly demonstrate controls such as restricted tool permissions, human escalation, audit trails, evaluation gates, and limits on automatic remediation.
- Research examples: Research-agent scripts use example source records for demonstrating evidence handling. Treat the included records as exercise data, not as independently verified research findings.
- CareerPilot distinction: The linked CareerPilot repository has its own React/TypeScript frontend and FastAPI/PostgreSQL backend. Those technologies describe CareerPilot, not the standalone Python lab scripts in this archive.
Future Scope
