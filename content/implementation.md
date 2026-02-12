## Implementation
{:#implementation}

Comunica MCP SPARQL is a TypeScript/JavaScript project that builds upon the [Comunica SPARQL querying framework](cite:cites comunica).
It is open-source, available on [GitHub](https://github.com/comunica/comunica-feature-mcp/){:.mandatory}, the [npm package manager](https://npmjs.com/package/@comunica/mcp-sparql){:.mandatory},
and is available under the MIT license.
Comunica is a modular SPARQL framwork that enables SPARQL querying over decentralized Knowledge Graphs.
This includes Knowledge Graphs exposed as [SPARQL endpoints](cite:cites spec:sparqlprot),
[Linked Data documents](cite:cites linkeddata) in any RDF representation, [TPF interfaces](cite:cites tpf), [HDT files](cite:cites hdt), [Solid pods](cite:cites solid), and more.
In contrast to GRASP, Comunica MCP SPARQL is exposed through the standardized MCP protocol instead of using direct function calling.
Furthermore, besides allowing the LLM agent to execute any possible query,
Comunica MCP SPARQL also dynamically allows the agent to provide one or more Knowledge Graph URL to query over.
And if the AI agent does not know what URLs to start from,
the engine can perform [link traversal](cite:cites linktraversalfoundations,solidquery) to discover relevant sources by following links.

Comunica MCP SPARQL is not the first MCP approach for SPARQL, but it has some notable differences to existing work.
Certain SPARQL engine vendors have their own dedicated MCP servers, such as
[Jena](https://github.com/ramuzes/mcp-jena){:.mandatory},
[GraphDB](https://graphdb.ontotext.com/documentation/11.1/using-graphdb-llm-tools-with-external-clients.html){:.mandatory},
and [Stardog](https://lobehub.com/mcp/vairpower-stardog_graphrag_mcp_poc){:.mandatory}.
These MCP servers are tied to these systems, while Comunica MCP SPARQL works with any Knowledge Graph.
Furthermore, [RDF Explorer](https://github.com/emekaokoye/mcp-rdf-explorer){:.mandatory} and [SPARQL-MCP](cite:cites sparqlmcp) are not tied to specific Knowledge Graphs,
but in contrast to Comunica MCP SPARQL,
they only handles Knowledge Graphs exposed through SPARQL endpoints.
SPARQL-MCP is the only tool that also supports federation,
but in contrast to Comunica MCP SPARQL,
it requires the LLM agent to explicitly include `SERVICE` keywords within the query,
while Comunica assigns these automatically and offers virtually integrated Knowledge Graph access.

TODO: explain tools...
{:.todo}