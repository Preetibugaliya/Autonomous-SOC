# 🛡️ Autonomous SOC System

### AI-Powered Security Operations Center with Multi-Agent Automation

---

## 📌 Overview

The **Autonomous SOC System** is a fully containerized, AI-driven Security Operations Center (SOC) designed to simulate real-world cyber defense workflows. It integrates multiple services such as attack simulation, log collection, threat detection, AI-based analysis, and automated response mechanisms.

This project demonstrates how modern SOC environments can leverage **AI agents, workflow orchestration, and automation tools** to detect, analyze, and respond to cyber threats in real time.

---

## 👨‍💻 Team Details

**Team Name:** Cyber Crew

**Team Members:**

* Vansh Khandelwal (2024/19229)
* Raghav Sharma (2024/17861)
* Preeti Bugaliya (2024/17680)

---

## 🚀 Key Features

* 🔐 Simulated attack environment using client container
* 📊 Centralized log collection and monitoring
* 🚨 Real-time threat detection engine
* 🤖 AI-powered multi-agent SOC workflow
* ⚙️ Automated incident response system
* 📈 Live dashboard visualization
* 🔄 Workflow orchestration using n8n

---

## 🏗️ System Architecture

The system consists of multiple interconnected services working together:

* **Client:** Simulates cyber attacks
* **Auth Server:** SSH-based target system generating logs
* **Log Collector:** Aggregates logs from all services
* **Detection Engine:** Identifies suspicious patterns
* **AI Agents:** Perform analysis using multi-agent workflows
* **Response Engine:** Executes automated response actions
* **Dashboard:** Displays real-time SOC data
* **n8n:** Handles workflow automation and orchestration

---

## ⚙️ Docker-Based Infrastructure

The entire system is orchestrated using Docker Compose, ensuring scalability and easy deployment. 

Each service runs in its own container and communicates through a shared network (`soc-network`).

---

## 📡 Services and Ports

| Service          | Port | Description                  |
| ---------------- | ---- | ---------------------------- |
| Dashboard        | 8080 | Web interface for monitoring |
| n8n              | 5678 | Workflow automation tool     |
| Log Collector    | 5000 | Central log ingestion        |
| Detection Engine | 5001 | Threat detection service     |
| AI Agents        | 5002 | AI-based analysis agents     |
| Response Engine  | 5003 | Automated response system    |
| Auth Server      | 2222 | SSH attack target            |

---

## ⚡ Quick Start Guide

### 1. Set API Key

Before starting the system, set your API key:

```bash
export ANTHROPIC_API_KEY='your-anthropic-api-key'
```

---

### 2. Start the System

Run the startup script:

```bash
./start.sh
```

This script builds and launches all containers. 

---

### 3. Access the Dashboard

* Main Dashboard → http://localhost:8080
* n8n Workflow UI → http://localhost:5678

  * Username: `admin`
  * Password: `admin123`

---

### 4. Run Attack Simulation

To simulate a cyber attack:

```bash
./attack.sh
```

This executes the attack inside the client container. 

---

## 🔄 Workflow Explanation

1. Attack is executed from the client
2. Logs are generated and collected
3. Detection engine analyzes logs
4. Alerts are sent to n8n
5. n8n triggers AI agents:

   * Triage Agent (Initial analysis)
   * Investigation Agent
   * Threat Intelligence Agent
   * Decision Agent (SOC Lead)
   * Response Agent
   * Reporting Agent
6. Response engine takes action
7. Dashboard updates in real time

---

## 🛠️ Useful Commands

```bash
./start.sh       # Start all services
./stop.sh        # Stop all services
./attack.sh      # Run attack simulation
./logs.sh        # View system logs
docker-compose ps  # Check running containers
```

* Log viewing uses Docker logs streaming. 
* Stop script shuts down all containers. 

---

## 🔗 n8n Workflow Setup

1. Open http://localhost:5678
2. Login using admin credentials
3. Import workflow from:

   ```
   n8n-workflows/soc-workflow.json
   ```
4. Activate the workflow

---

## 📂 Project Structure

```
autonomous-soc/
├── containers/              # Docker service containers
│   ├── client/             # Attack simulator
│   ├── auth-server/        # SSH server
│   ├── log-collector/      # Log aggregation
│   ├── detection-engine/   # Threat detection
│   ├── ai-agents/          # AI SOC agents
│   ├── response-engine/    # Automated response
│   └── dashboard/          # Web dashboard
├── logs/                   # Log files
├── n8n-workflows/          # Workflow definitions
├── docker-compose.yml      # Container orchestration
├── start.sh                # Start script
├── stop.sh                 # Stop script
├── attack.sh               # Attack simulation
├── logs.sh                 # Log viewer
└── README.md               # Project documentation
```

---

## 🎯 Learning Outcomes

This project helps in understanding:

* SOC architecture and workflows
* Threat detection and incident response
* AI integration in cybersecurity
* Docker-based system design
* Automation using workflow engines

---


## ⭐ Conclusion

The Autonomous SOC System showcases how modern cybersecurity operations can be automated using AI and containerized microservices. It serves as a practical implementation of a **next-generation SOC environment**, combining detection, analysis, and response into a seamless workflow.

---
