# AI Pipeline Failure Root Cause Assistant

## Overview

AI Pipeline Failure Root Cause Assistant is an AI-powered DataOps solution that automates pipeline failure investigation using Retrieval Augmented Generation (RAG), vector search, and workflow automation.

The system analyzes failed pipeline logs, retrieves similar historical incidents from a vector database, generates AI-powered Root Cause Analysis (RCA), and automatically notifies stakeholders.

---

## Problem Statement

Enterprise ETL and data pipelines frequently fail due to:

* Missing source files
* Schema mismatches
* API failures
* SFTP/XML ingestion issues
* Warehouse load failures
* Authentication problems
* Data quality issues

Today, Data Operations Engineers spend 2–5 hours manually:

* Analyzing logs
* Searching historical incidents
* Identifying root causes
* Preparing RCA reports

This process is repetitive, time-consuming, and operationally expensive.

---

## Solution

This project automates pipeline failure investigation using:

* Gemini AI
* Pinecone Vector Database
* RAG Architecture
* n8n Workflow Automation

The system:

1. Captures failed pipeline logs
2. Generates embeddings using Gemini AI
3. Searches historical incidents using Pinecone
4. Retrieves similar past failures
5. Generates AI-powered RCA
6. Sends automated Gmail alerts

---

## Architecture

```text
Pipeline Failure
        ↓
Webhook Trigger
        ↓
Gemini Embeddings
        ↓
Pinecone Vector Search
        ↓
Historical Incident Retrieval
        ↓
AI RCA Generation
        ↓
Automated Gmail Alert
```

---

## Tech Stack

| Component           | Technology |
| ------------------- | ---------- |
| Workflow Automation | n8n        |
| AI Model            | Gemini AI  |
| Vector Database     | Pinecone   |
| Notifications       | Gmail API  |
| Trigger Mechanism   | Webhooks   |
| Scripting           | JavaScript |

---

## Key Features

* AI-powered Root Cause Analysis
* Retrieval Augmented Generation (RAG)
* Semantic similarity search
* Historical incident retrieval
* Automated email notifications
* Enterprise DataOps automation
* Low-code workflow orchestration

---

## Repository Structure

```text
AI-Pipeline-Failure-Root-Cause-Assistant/

├── workflows/
│   ├── workflow1_historical_incident_ingestion.json
│   └── workflow2_pipeline_failure_rca.json
│
├── docs/
│   ├── Architecture_Diagram.png
│   ├── Presentation.pptx
│   └── Problem_Statement.pdf
│
├── screenshots/
│   ├── workflow.png
│   ├── pinecone_query.png
│   ├── rca_output.png
│   └── gmail_alert.png
│
├── sample-data/
│   ├── historical_incidents.json
│   └── failed_log.json
│
└── README.md
```

---

## Credentials Setup

Configure the following credentials inside n8n Credential Manager:

* YOUR_GEMINI_API_KEY
* YOUR_PINECONE_API_KEY
* YOUR_PINECONE_INDEX_HOST
* [YOUR_EMAIL@gmail.com](mailto:YOUR_EMAIL@gmail.com)

⚠️ Do not commit API keys, tokens, or credential files to GitHub.

---

## Sample Workflow

### Historical Incident Ingestion

* Reads historical incidents
* Generates embeddings
* Stores vectors in Pinecone

### Pipeline Failure RCA

* Receives failed pipeline logs
* Retrieves similar incidents
* Generates RCA
* Sends email notifications

---

## Business Impact

| Metric                 | Before    | After       |
| ---------------------- | --------- | ----------- |
| RCA Investigation      | 2–5 Hours | < 3 Minutes |
| Incident Lookup        | Manual    | Automated   |
| Operational Efficiency | Low       | High        |
| MTTR                   | High      | Reduced     |

---

## Future Enhancements

* Slack Integration
* Microsoft Teams Alerts
* Predictive Failure Detection
* Auto-Remediation Workflows
* Airflow Integration
* Databricks Integration

---

## Author

Built as part of the Be10X AI Generalist Hackathon.

Focused on applying AI, RAG, and workflow automation to solve real-world DataOps challenges.
