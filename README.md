# Research-Agent-using-LangGraph
### 🧠 Wikipedia Research Agent using GPT-3.5 + LangGraph

This project implements an interactive **AI research assistant** that can:
- Search Wikipedia for a given topic
- Summarize the information using OpenAI's GPT-3.5
- Handle errors in a structured, stateful way using a LangGraph execution flow

---

## 🚀 Features

 Searches Wikipedia using `WikipediaAPIWrapper`  
 Summarizes results with `ChatOpenAI` (GPT-3.5 Turbo)  
 Tracks state with a custom `ResearchState` class  
 Manages flow using `LangGraph` state machine  
 Logs a full conversation history  
 Handles errors and fallback scenarios gracefully

---
## 🧭 State Graph Architecture

<img width="429" height="656" alt="image" src="https://github.com/user-attachments/assets/9a2beef7-d982-4f1c-a969-1a54d2fcc07e" />


  Each step in the graph represents a processing stage:
  
  - search: Pulls content from Wikipedia
  
  - summarize: Uses GPT-3.5 to create a summary
  
  - handle_error: Fallback if any step fails

## Sample Output
Enter your research topic: LangChain

--- Conversation ---

User: LangChain

Agent: Found information from Wikipedia about 'LangChain'. Summarizing...

Agent: LangChain is a framework for building LLM-powered applications...

Final Summary:

LangChain is a modular framework designed for developing apps with language models...




