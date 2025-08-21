# Multi-Agent Financial & Web Search AI

## Project Overview

This project demonstrates a **multi-agent AI system** that combines web search and financial analysis capabilities using the Groq LLM (`llama-3.3-70b-versatile`). It integrates two specialized agents:

1. **Web Search Agent** – Searches the internet using DuckDuckGo to gather relevant information.
2. **Finance AI Agent** – Accesses financial data using Yahoo Finance tools to provide stock prices, analyst recommendations, company news, and fundamentals.

The agents are orchestrated into a **multi-agent setup** that allows them to collaborate and provide enriched responses.

---

## Features

- **Web Search Agent**
  - Searches the web for requested information.
  - Always includes sources in its responses.
  - Supports streaming responses for real-time output.

- **Finance AI Agent**
  - Retrieves stock prices, analyst recommendations, company news, and financial fundamentals.
  - Uses tables to neatly display structured data.
  - Integrates seamlessly with the web search agent in a multi-agent system.

- **Multi-Agent Collaboration**
  - Combines insights from both web search and financial agents.
  - Produces well-structured, source-backed summaries.
  - Streaming response capability for real-time interaction.

---

## Technology Stack

- **Language:** Python 3.12  
- **Libraries / Frameworks:**  
  - `phi` (for multi-agent orchestration)  
  - `Groq` (LLM backend)  
  - `YFinanceTools` (financial data retrieval)  
  - `DuckDuckGo` (web search tool)  

- **Model:** `llama-3.3-70b-versatile` (Groq LLM supporting tool use)

---

## How It Works

1. **Web Search Agent** is initialized with DuckDuckGo to fetch general web information.  
2. **Finance AI Agent** is initialized with Yahoo Finance tools to gather structured financial data.  
3. Both agents are combined into a **multi-agent system**, which takes a single query and decides which agent to invoke for which part of the response.  
4. The `print_response` function streams a combined, formatted response containing both financial insights and web search results.

**Example Query:**

```python
multi_ai_agent.print_response(
    "Summarize analyst recommendations and share the latest news for NVDA",
    stream=True
)
```

```bash
pip install -r requirements.txt
```
```bash
export GROQ_API_KEY="your_api_key_here"
```
```bash
python financial_agent.py
```

### Future Improvements
#### Enhance the multi-agent orchestration logic for more complex workflows.


### Thanks!