
# AgentTrust: Trust-Aware Authorization and Behavioral Anomaly Detection for Multi-Agent AI Systems

## 1. Project Information

| Field | Details |
|---|---|
| Course ID | 21CSC203P |
| Course Name | Advanced Programming Practices |
| Subject Category | APP |
| Project Title | AgentTrust |
| Team Leader | Dhanish K |
| Register Number | RA2511003050241 |
| Department | CSE |
| Section | E |
| Academic Year | Second Year |
| Mentor | Dr. S. Shargunam |

## 2. Project Overview

AgentTrust is a security and trust-management layer for multi-agent AI systems. It is designed to evaluate agent actions before execution and monitor agent behaviour for potentially anomalous activity.

The project combines an authorization engine with a behavioural-analysis component. The authorization layer manages agent identities, permissions, policies, contextual checks, risk evaluation, trust scores, delegation controls, human oversight, and audit monitoring.

The behavioural-analysis component evaluates agent events using multiple detectors and an analysis pipeline.

The project also includes Finance, Data, and Supervisor agents, along with a FastAPI-based demonstration interface.

## 3. Problem Statement

Multi-agent AI applications may delegate tasks and invoke tools across different agents. Without appropriate security controls, an agent may attempt actions beyond its intended permissions, delegate work inappropriately, or exhibit unusual behavioural patterns.

AgentTrust addresses this challenge by exploring a layered security approach that combines identity-based authorization, policy evaluation, trust management, delegation controls, and behavioural anomaly detection.

## 4. Project Objectives

1. Develop a centralized authorization mechanism for multi-agent AI systems.
2. Register agents with specific identities, roles, and permissions.
3. Evaluate agent requests using configured access-control policies.
4. Incorporate contextual and risk-related checks into authorization decisions.
5. Implement trust management and delegation controls.
6. Analyse agent events to identify unusual behavioural patterns.
7. Provide human oversight and audit monitoring mechanisms.
8. Demonstrate the security framework through cooperating AI agents and a web interface.

## 5. System Architecture

### 5.1 Agent Authorization Module

Location: `agenttrust/agent_auth/`

This module contains the core authorization components:

- Identity Manager
- Authorization Engine
- Policy Management
- Context Analyzer
- Behaviour Analyzer
- Risk Evaluator
- Trust Manager
- Delegation Control
- Human Oversight
- Audit Monitor
- Data Store

### 5.2 Behaviour Analyzer

Location: `agenttrust/behavior_analyzer/`

This module provides behavioural anomaly detection through:

- Event analysis pipeline
- Detector registry
- Baseline management
- Delegation detection
- Frequency detection
- Parameter analysis
- Statistical detection
- Temporal detection
- Isolation Forest-based detection
- Result aggregation
- Data storage components

### 5.3 Finance Agent

Location: `finance_agent/`

The Finance Agent handles invoice-related operations using mock invoice data and provides invoice search functionality.

### 5.4 Data Agent

Location: `data_agent/`

The Data Agent handles customer-related operations, including customer searches and retrieval of customer details.

### 5.5 Supervisor Agent

Location: `supervisor_agent/`

The Supervisor Agent coordinates tasks between multiple agents and manages the execution of assigned operations.

### 5.6 Security Gateway

File: `agenttrust/gateway.py`

The security gateway intercepts tool calls and routes them through the authorization engine. It evaluates requests before allowing or denying the execution of protected functions.

### 5.7 Web Application

File: `web_app.py`

The project includes a FastAPI-based web application with a frontend built using HTML, CSS, and JavaScript.

The interface provides demonstration workflows and behavioural-analysis functionality.

## 6. Repository Structure

```text
AgentTrust/
├── agenttrust/
│   ├── agent_auth/
│   ├── behavior_analyzer/
│   │   ├── baseline/
│   │   ├── core/
│   │   ├── detectors/
│   │   ├── models/
│   │   ├── scoring/
│   │   ├── store/
│   │   └── tests/
│   └── gateway.py
├── finance_agent/
├── data_agent/
├── supervisor_agent/
├── tests/
├── static/
├── agent_behavior_dataset.json
├── demo_orchestration.py
├── generate_dataset.py
├── presentation.py
├── run_data_agent.py
├── run_finance_agent.py
├── train_and_demo.py
├── verify_langchain.py
├── web_app.py
├── requirements.txt
└── README.md
```

## 7. Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| LangChain | Agent and tool integration |
| FastAPI | Backend web application |
| Uvicorn | Application server |
| Pytest | Software testing |
| JSON | Dataset and demonstration data |
| HTML | Frontend structure |
| CSS | Frontend styling |
| JavaScript | Frontend functionality |
| Isolation Forest | Behavioural anomaly detection |

## 8. Installation and Setup

### Prerequisites

- Python installed on the system.
- Git installed on the system.
- Visual Studio Code or another code editor.
- Terminal or command prompt.

### Step 1: Clone the Repository

```bash
git clone https://github.com/dhanish1505/RA2511003050241_APP_Project_Nov_26.git
cd RA2511003050241_APP_Project_Nov_26
```

### Step 2: Create a Virtual Environment

Windows:

```powershell
python -m venv .venv
```

### Step 3: Activate the Virtual Environment

Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### Step 4: Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

Note: Ensure that all runtime dependencies imported by the application are installed and listed in requirements.txt.

## 9. Running the Project

### Run the Finance Agent

```bash
python run_finance_agent.py
```

### Run the Data Agent

```bash
python run_data_agent.py
```

### Run the Supervisor Demonstration

```bash
python demo_orchestration.py
```

### Run the Web Application

```bash
python web_app.py
```

After successful startup, open the following address in your browser:

```text
http://127.0.0.1:8000
```

### Verify the Environment

```bash
python verify_langchain.py
```

## 10. Behavioural Dataset and Analysis

The repository includes an agent behavioural dataset named `agent_behavior_dataset.json`.

The web application reads the dataset, converts the records into agent events, and submits them to the Behaviour Analyzer.

The behavioural-analysis module uses multiple detection mechanisms to examine agent activity and identify potentially unusual patterns.

## 11. Testing

Run the main test suite:

```bash
python -m pytest tests/ -v
```

Run behavioural analyzer tests:

```bash
python -m pytest agenttrust/behavior_analyzer/tests/ -v
```

## 12. Team Members

| S. No. | Full Name | Register Number | Department | Section | Academic Year | Role |
|---|---|---|---|---|---|---|
| 1 | Dhanish K | RA2511003050241 | CSE | E | Second Year | Team Leader |
| 2 | Sritharan S | RA2511003050275 | CSE | E | Second Year | Team Member |
| 3 | Jeffriash T | RA2511003050294 | CSE | E | Second Year | Team Member |
| 4 | Dharshini V | RA2511003050286 | CSE | E | Second Year | Team Member |

## 13. Mentor Details

- Mentor Name: Dr. S. Shargunam
- Designation: Not provided

## 14. Project Report

The final project report is included as a PDF document in the root directory of the repository.

Recommended filename:

`AgentTrust_Project_Report.pdf`

## 15. Academic Submission Details

**Course ID:** 21CSC203P

**Course Name:** Advanced Programming Practices

**Project Title:** AgentTrust

**Submission Category:** APP

**Team Leader:** Dhanish K

**Register Number:** RA2511003050241

**Mentor:** Dr. S. Shargunam

_____
**Developed as part of the Advanced Programming Practices course (21CSC203P).**

**Project: AgentTrust | Academic Year: Second Year | Department: CSE – E**
