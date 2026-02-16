## Conclusions
{:#conclusions}

MCP enables AI agents to act as orchestrators of other systems,
and Comunica MCP SPARQL offers this connection point to Knowledge Graphs.
Thanks to the power of [Comunica](cite:cites comunica),
not just SPARQL endpoints can be queried, but also Linked Data documents in any RDF serialization, Solid pods (including authenticated access to private data), and more.
And if the agent does not know what data sources to start from, Comunica's [link traversal engine](cite:cites solidquery) can be used.

Our preliminary findings show that modern LLMs mostly seem to decide to query over DBpedia and Wikidata, which they do very well.
This confirms earlier experments that show that [LLMs internalize DBpedia and Wikidata during pretraining](cite:cites internalizedwikidatadbpedia).
If the user wants to query over other Knowledge Graphs (such as Uniprot or DBLP), they need to ask it explicitly.
Furthermore, LLMs seem to struggle with writing federated queries, and can even hallucinate SPARQL endpoint URLs.
For this, Comunica MCP SPARQL is a tool that acts as an enabler for future research.
For instance, there is a need for more research on how well agents can understand other Knowledge Graphs besides DBpedia and Wikidata,
for which exposing additional tools in line with those of [GRASP](cite:cites grasp) could be valuable.
Furthermore, more research is needed on guiding agents towards query-relevant Knowledge Graphs,
similar to the work set out by the authors of [SPARQL-MCP](cite:cites sparqlmcp).
