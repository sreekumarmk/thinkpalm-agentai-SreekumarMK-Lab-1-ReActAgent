# Simple Chat Agent with LangChain and Groq

This repository contains a notebook-based demo of a simple ReAct-style chat agent built with LangChain and the Groq LLM.

## Overview

The project demonstrates how to use:

- `langchain` and `langchain-core` for agent orchestration
- `langchain-groq` to connect to Groq's chat model
- `ddgs` for live web search through DuckDuckGo
- a custom ReAct prompt to enforce step-by-step reasoning and tool usage

## Features

- Calculator tool for evaluating expressions
- Web search tool for retrieving current information
- Strict `Thought / Action / Observation / Final Answer` ReAct flow
- Output cleaning logic to extract the final answer text

## Files

- `src/SimpleChatAgentUsingLangChainAndGroq.ipynb` - Jupyter Notebook implementing the agent

## Setup

1. Install required packages.

```bash
pip install -q --upgrade langchain langchain-core langchain-community langchain-groq ddgs
```

2. Set your Groq API key.

```bash
export GROQ_API_KEY="YOUR_GROQ_API_KEY"
```

3. Open the notebook in Jupyter or VS Code and run the cells.

## Usage

- Run the notebook cells in order.
- The agent is configured to accept user input in a loop.
- Type questions or commands in the notebook prompt.
- Enter `exit` to quit the loop.

## Notes

- The notebook uses a free-tier friendly Groq model: `llama-3.1-8b-instant`.
- The agent is designed to produce plain-text final answers only, without Markdown or special formatting.
- The web search tool uses DuckDuckGo Search via the `ddgs` package, limited to the top 3 results.

## License

Feel free to adapt this demo for experimentation and learning.
