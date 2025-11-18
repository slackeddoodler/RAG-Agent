# **MCP + GroundX Document Intelligence Server**

A lightweight MCP server powered by **EyeLevelAI’s GroundX** for advanced document parsing, search, and retrieval.
Use it directly inside **Cursor IDE** or **VS Code with GitHub Copilot** as an MCP client.

---

## 🚀 **Tech Stack**

* **Cursor IDE** or **VS Code (GitHub Copilot MCP)** — MCP client
* **FastMCP** — to build the local MCP server
* **EyeLevelAI GroundX** — enterprise-grade document parsing + search over complex docs (text, images, tables, diagrams)

---

## 🧠 **How It Works**

1. User interacts with the MCP client (Cursor / VS Code).
2. Client connects to the MCP server and loads available tools.
3. Tools call **GroundX** to ingest or search documents.
4. GroundX parses complex docs (text, tables, images, diagrams) into structured JSON.
5. The MCP client uses the results to generate accurate responses and RAG-style outputs.

---

## **What This Project Does**

This project builds an MCP server that uses **EyeLevelAI’s GroundX** to ingest and search complex real-world documents. The user interacts through Cursor or VS Code, and the MCP client connects to the server to run tools that upload documents, parse them into structured JSON, and perform advanced semantic search. GroundX handles the heavy lifting—extracting text, tables, images, diagrams, and other multimodal content—so the client can generate accurate, context-aware responses over ingested documents.

---

## Setup Instructions:

1. Install dependencies:

```bash
pip install fastmcp groundx
```

Your `groundx_client.py` should initialize a **FastMCP** server and register both tools (ingestion + search).

---

2. Download the `groundx_client.py` file.

---

3. Get an API key from EyeLevelAI and store it in `.env`:

```
GROUNDX_API_KEY=your_key_here
```

Your `groundx_client.py` will expose:

* `ingest_document(path)`
* `search(query)`

---

4. Choose any PDF, place it inside the `docs/` folder, pass its file path during input, and then give another input to query across your uploaded documents.

---

5. Connect to Cursor or Github Copilot in VS Code

Inside your Cursor IDE:

```
Cursor → Settings → Cursor Settings → MCP
```

Add the MCP server and point it to your `groundx_client.py`.

---

## 💡 Why We Use EyeLevelAI GroundX

GroundX offers powerful enterprise-grade parsing systems capable of handling text, tables, images, equations, and diagrams.
It converts unstructured documents into structured JSON that LLMs can easily use to build high-quality RAG systems.
