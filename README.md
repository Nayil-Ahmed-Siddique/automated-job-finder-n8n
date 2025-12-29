# automated-job-finder-n8n

flowchart LR
    A[Schedule Trigger] --> B1[RSS Read 1]
    A --> B2[RSS Read 2]
    A --> B3[RSS Read 3]

    B1 --> C[Merge Feeds]
    B2 --> C
    B3 --> C

    C --> D[Filter: Software Jobs]
    D --> E[Filter: Country]
    E --> F[Job Scoring Logic]
    F --> G[Quality Filter]
    G --> H[Prepare Email Content]
    H --> I[Send Email Alert]

📌 Automated Job Finder – Email Alerts (n8n)
🔍 Overview

This project is an automation workflow built using n8n that continuously monitors multiple job boards via RSS feeds, filters relevant software engineering roles, scores job quality, and delivers curated job alerts via email.

The goal of this project is to demonstrate real-world automation design, data aggregation, filtering logic, and workflow orchestration.

⚙️ How It Works

Schedule Trigger

Runs the workflow automatically at defined intervals.

Multiple RSS Feeds

Pulls job listings from several high-volume job sources simultaneously.

Merge Node

Aggregates all job feeds into a single unified stream.

Job Filtering

Filters roles based on keywords such as:

Software Engineer

Developer

Backend / Frontend

Applies optional country-based filtering.

Job Scoring Logic

Assigns a quality score to each job based on relevance.

Quality Gate

Ensures only high-quality, relevant jobs pass through.

Email Automation

Formats job listings into a structured email.

Sends job alerts automatically.

🧠 Why This Project Matters

This workflow demonstrates:

Practical automation design

Event-driven workflows

Data aggregation from multiple sources

Conditional logic and filtering

Real-world email alert systems

It mirrors how production automation systems are built for monitoring, alerting, and content delivery.

🛠️ Tech Stack

n8n – Workflow automation

RSS Feeds – Data ingestion

JavaScript (Code Nodes) – Custom logic & scoring

Email Integration – Automated notifications

📊 Workflow Diagram

or

flowchart LR
    A[Schedule Trigger] --> B1[RSS Read 1]
    A --> B2[RSS Read 2]
    A --> B3[RSS Read 3]

    B1 --> C[Merge Feeds]
    B2 --> C
    B3 --> C

    C --> D[Filter: Software Jobs]
    D --> E[Filter: Country]
    E --> F[Job Scoring Logic]
    F --> G[Quality Filter]
    G --> H[Prepare Email Content]
    H --> I[Send Email Alert]

🚀 Getting Started

Import the workflow JSON into n8n

Configure:

RSS feed URLs

Email credentials

Activate the workflow

Sit back and let automation do the work

📌 Use Case Examples

Job monitoring systems

Market intelligence automation

Content aggregation pipelines

Alerting & notification workflows
