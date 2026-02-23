## Introduction
{:#introduction}

The paradigm of [neuro-symbolic artificial intelligence](cite:cites neurosymbolicai)
aims to integrate symbolic reasoning with machine learning,
to improve overall accuracy, trustworthiness, and explainability.
[Graph-based retrieval augmented generation (GraphRAG)](cite:cites graphrag) offers one approach to achieve neuro-symbolic AI
by combining vector embedding-based semantic retrieval with explicit graph structures such as Knowledge Graphs
for guiding answers from Large Language Models (LLMs) through vector search.
GraphRAG techniques involve embedding generation for specific Knowledge Graphs.
This means that LLMs can not directly incorporate arbitrary Knowledge Graphs without preprocessing them first.
The zero-shot approach for SPARQL-based question answering introduced in [GRASP](cite:cites grasp)
offers one solution of this problem,
which offers functions that can be called by LLM agents to interact with a Knowledge Graph.

Recently, the [Model Context Protocol (MCP)](cite:cites mcp) was introduced that allows LLM agents to connect to external systems.
Concretely, it allows MCP servers to offer specific *tools* that can produce a certain output based on various parameters.
These tools are described externally in a human-readable format to the LLM,
and internally connects to specific systems such as the file system, code editors, or databases.
One main advantage of MCP is that it runs over live systems, and does not require embedding-like precomputions.
Conversely, Comunica MCP requires a remotely or locally running MCP server alongside a Comunica engine, which contradicts Comunica's goal to push execution to the client.
Addressing this limitation, [webMCP](cite:cites webmcp), a recent W3C community group report pushed by Microsoft and Google, proposes bringing MCP capabilities directly into the browser by enabling web pages to register available tools through the `navigator.modelContext` interface.
As such, it offers an excellent opportunity for connecting arbitrary Knowledge Graphs on the fly.
Within this demonstration, we introduce Comunica MCP SPARQL, providing a connection point between LLMS and Comunica, and show how it works.
Additionally, we demonstrate how webMCP within
[Comunica's web UI](https://query.comunica.dev/){:.mandatory}
can bring MCP to the browser.
