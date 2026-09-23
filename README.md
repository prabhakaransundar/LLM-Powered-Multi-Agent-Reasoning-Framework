# 🤖 LLM-Powered Multi-Agent Reasoning Framework

> An AI-powered analytics assistant that allows users to explore datasets using natural language instead of writing SQL or Python manually.

## Overview

**AI Data Analyst Agent** is an intelligent data analysis application designed to simplify the process of exploring structured datasets.

Users can upload a CSV or Excel file and ask questions such as:

* "Which product generated the highest revenue?"
* "Show me the monthly sales trend."
* "What are the top 5 categories?"
* "Are there any unusual values in the dataset?"
* "Summarize the key business insights."

The system interprets the user's request, selects the appropriate analysis tool, executes the required operations, and returns an easy-to-understand response.

---

## ⚡ What It Can Do

### Natural Language Analysis

Ask questions about your data without writing SQL or Python.

### Automated Data Exploration

The agent can inspect:

* Columns and data types
* Missing values
* Duplicate records
* Statistical summaries
* Relationships between variables

### SQL & Python Analysis

Depending on the query, the system can use SQL or Python-based analysis to retrieve and process information.

### Visualization Generation

Automatically generate charts for questions involving:

* Trends
* Comparisons
* Distributions
* Category performance
* Correlations

### AI-Powered Insights

Instead of returning raw numbers, the agent converts analytical results into concise business insights.

### Conversational Follow-ups

Users can continue asking questions about the same dataset without restarting the analysis.

---

## 🧠 System Architecture

```text
                    User
                     │
                     ▼
             Natural Language Query
                     │
                     ▼
              ┌───────────────┐
              │   AI Agent    │
              └───────┬───────┘
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
       SQL Tool   Python Tool   Visualization
          │           │           │
          └───────────┼───────────┘
                      ▼
               Analysis Results
                      │
                      ▼
               LLM Explanation
                      │
                      ▼
                User Response
```

---

## 🛠️ Technology Stack

| Layer            | Technology      |
| ---------------- | --------------- |
| Programming      | Python          |
| AI / LLM         | OpenAI / Gemini |
| Agent Framework  | LangGraph       |
| Data Processing  | Pandas          |
| Database         | PostgreSQL      |
| Vector Search    | pgvector        |
| API              | FastAPI         |
| Visualization    | Plotly          |
| UI               | Streamlit       |
| Containerization | Docker          |

---

## 📁 Project Structure

```text
ai-data-analyst-agent/
│
├── app/
│   ├── agents/
│   │   ├── analyst.py
│   │   └── planner.py
│   │
│   ├── tools/
│   │   ├── sql_tool.py
│   │   ├── python_tool.py
│   │   └── visualization.py
│   │
│   ├── services/
│   │   ├── data_loader.py
│   │   └── insight_generator.py
│   │
│   ├── api/
│   │   └── routes.py
│   │
│   └── config.py
│
├── data/
│   └── sample_data.csv
│
├── notebooks/
│   └── experimentation.ipynb
│
├── tests/
│
├── .env.example
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
└── README.md
```

---

## 🔄 How It Works

### 1. Upload Dataset

The user uploads a CSV or Excel dataset through the application.

### 2. Dataset Profiling

The system identifies:

* Available columns
* Data types
* Missing values
* Duplicate records
* Basic statistics

### 3. Query Understanding

The LLM interprets the user's question and determines what type of analysis is required.

### 4. Tool Selection

The agent selects an appropriate tool:

```text
Business Question
       ↓
   AI Planner
       ↓
 ┌─────┴─────┐
 ▼           ▼
SQL       Python
 │           │
 └─────┬─────┘
       ▼
   Result
```

### 5. Result Validation

The generated result is checked before being passed to the response generation layer.

### 6. Insight Generation

The LLM converts the analytical result into a concise explanation that a business user can understand.

---

## 💬 Example

**User**

> Which category generated the most revenue?

**Agent**

```text
1. Identify revenue-related columns
2. Calculate quantity × price
3. Group revenue by category
4. Sort categories by revenue
5. Generate visualization
6. Explain the result
```

**Response**

> Electronics generated the highest revenue during the analyzed period, contributing approximately 34% of total sales.

---

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/ai-data-analyst-agent.git

cd ai-data-analyst-agent
```

### Create a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```bash
venv\Scripts\activate
```

**macOS / Linux**

```bash
source venv/bin/activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Configure environment variables

Create a `.env` file:

```env
OPENAI_API_KEY=your_api_key
DATABASE_URL=your_database_url
```

### Start the application

```bash
streamlit run app.py
```

---

## 🔐 Security Considerations

The application should never expose API keys directly in the source code.

Use environment variables for credentials and avoid committing `.env` files to the repository.

```text
.env
```

should be included in `.gitignore`.

GitHub also recommends using repository security features such as secret scanning and push protection for public repositories.

---

## 📌 Future Improvements

* [ ] Multi-dataset conversations
* [ ] Advanced chart recommendations
* [ ] Automatic anomaly detection
* [ ] Query history
* [ ] User authentication
* [ ] LLM response evaluation
* [ ] Agent observability and tracing
* [ ] Support for larger datasets
* [ ] Deployment with Docker
* [ ] Cloud deployment

---

## 🎯 Project Objective

The goal of this project is to combine **Generative AI, Agentic Workflows, Data Analytics and Software Engineering** into a practical application capable of assisting users with real-world data analysis.

---

## 👨‍💻 Author

**Prabhakaran Sundar**

AI Developer | Data Analyst

Skills demonstrated:

`Python` · `SQL` · `LLMs` · `LangGraph` · `RAG` · `Pandas` · `FastAPI` · `PostgreSQL` · `Plotly` · `Docker`

---

## 📄 License

This project is intended for educational and portfolio purposes.
