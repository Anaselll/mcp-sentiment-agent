---
title: Mcp Sentiment
emoji: 👀
colorFrom: red
colorTo: green
sdk: gradio
sdk_version: 6.14.0
python_version: '3.13'
app_file: server/app.py
pinned: false
---
# MCP Sentiment Analyzer

A minimal Model Context Protocol (MCP) tool for sentiment analysis. This repository demonstrates how to expose a sentiment analysis function (using `TextBlob`) as an MCP server via Gradio, and how to consume it using an AI agent framework (`smolagents`).

## Project Overview

- **Server (`server/app.py`)**: A Gradio application that performs text sentiment analysis (polarity and subjectivity) using `TextBlob` and seamlessly exposes it as an MCP server.
- **Client (`client/app.py`)**: A `smolagents` `CodeAgent` that connects to the hosted MCP server over SSE, allowing an LLM to dynamically call the sentiment analysis tool during user interactions.
