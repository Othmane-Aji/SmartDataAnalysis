# Crewlytics

**A modular AI-powered platform for analyzing product datasets, spotting trends, and generating business-friendly insights.**

---

## Overview

Crewlytics is a multi-agent data analysis system built with Python, LangChain, LangGraph, and the Gemini API. It allows users to upload a dataset, define a business objective (e.g., "Find sales trends"), and receive a detailed analysis that includes summaries, statistics, and visual insights — all in plain, non-technical language.

### Key Capabilities

- Automatic data cleaning  
- Exploratory data analysis (EDA)  
- Detection of trends, correlations, and anomalies  
- Chart and report generation  
- Executive-level summaries  

All accessible through an intuitive web-based interface.

---

## How It Works

1. **Upload a Dataset**  
   Supported formats: `.csv`, `.xlsx`, `.json` (up to 200MB)

2. **Define an Analysis Goal** *(Optional)*  
   Input a natural language prompt (e.g., “Analyze customer satisfaction”)

3. **Run the AI Workflow**  
   Behind the scenes, a LangGraph-driven agent crew performs:
   - Data cleaning  
   - EDA with visualizations  
   - Insight generation and reporting

4. **View Results**
   - Cleaned data preview  
   - Auto-generated charts  
   - Executive summary  
   - Option to download full PDF report

---

## Insight Generation Prompt

The summarization agent is driven by a structured prompt like:

> "You are a data analyst assistant. Based on the uploaded dataset and the EDA results, write a clear, professional summary that highlights key patterns, trends, correlations, and anomalies in plain business language."

---

## Project Structure

```bash
.
├── .langgraph_api/       # LangGraph configuration files
├── agents/               # Agent-specific logic and prompts
├── configs/              # App and pipeline settings
├── data/                 # Uploaded or temporary datasets
├── outputs/              # Analysis results and reports
├── services/             # EDA, charting, and other utilities
├── ui/                   # User interface components (Gradio/Streamlit)
├── workflows/            # LangGraph pipeline definitions
├── run.py                # Application entrypoint
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
├── langgraph.json        # LangGraph workflow configuration
└── .env                  # Environment variables and API keys

## Technologies Used

- **LangChain** + **LangGraph** for multi-agent orchestration
- **Gemini API** for natural language insight generation
- **Pandas / Seaborn / Matplotlib** for EDA and visualization
- **Gradio / Streamlit** (or similar) for frontend interface
- **WeasyPrint / HTML2PDF** for report generation

---

## Installation
```bash
git clone https://github.com/your-repo/product-data-analyzer.git
cd product-data-analyzer
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt

```

## Configuration
1. **API Keys**: Set up your API keys in the `.env` file.
2. **LangGraph**: Configure your LangGraph settings in `.langgraph_api/`.
3. **Run the app**: Start the web interface with:



