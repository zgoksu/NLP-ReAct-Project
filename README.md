# NLP-ReAct-Project

This project aims to create a ReAct Agent which customized for the cybersecurity field that thinks, makes decisions, and solves problems using external resources, based on a Language Model (LLM) that provides static responses. The developed Command Analysis & Scoring Agent supports SOC (Security Operations Center) processes in performing critical tasks such as malicious command analysis, MITRE ATT&CK technical mapping, and risk scoring.
    
## Problem Definition
SOC analysts must examine thousands of logs, commands, and alarms daily. The following problems are particularly prominent:

- Rapid analysis of Base64 encoded PowerShell commands
- Detection of misuse of LOLBAS binaries
- Determining whether individual events constitute an attack chain
- The need for risk scoring to prioritize events

This project aims to develop a ReAct-based cybersecurity agent that can solve these problems.

## Project Design
The primary objective is to evaluate the malicious potential of terminal commands and log sequences by correlating them with MITRE ATT&CK and LOLBAS knowledge bases using RAG (Retrieval-Augmented Generation).
The model operates as an orchestrator that autonomously retrieves technical context through a command_intel tool and quantifies threat levels via a specialized calculate_risk_score function. By implementing a Thought → Action → Observation loop, the project focuses on identifying complex, multi-hop attack chains and providing data-driven security assessments rather than simple pattern matching.


## Installation
To run the project on your own computer, follow these steps:
1. Install Required Libraries: 
 - Type the following code into the terminal or command line:
```bash
pip install -r requirements.txt
```
2. Set the API Key
3. Launch the Application


## Usage
When you start the application, you can send a command or log sequence to the agent for analysis.

#### Example Query:
```bash
query(""" Analyze this command: powershell.exe -nop -w hidden -enc SQBFAFgAIAAoAE4AZQB3AC0ATwBiAGoAZQBjAHQAIA== """)
```
