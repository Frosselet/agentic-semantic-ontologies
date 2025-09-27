# Claude Code Configuration - Semantic Ontologies

## Project: Agentic Semantic Ontologies
Foundation layer providing OWL/RDF ontologies with SKOS taxonomies for semantic knowledge management.

### Scope
This repository contains the semantic foundation for the agentic data scraper ecosystem:
- OWL/RDF ontology definitions
- SKOS taxonomy structures
- SPARQL navigation examples
- Semantic validation schemas

### Key Files
- `ontologies/bridge/gist_dbc_bridge.owl` - Core business-data bridge ontology
- `ontologies/sow/complete_sow_ontology.owl` - Statement of Work ontology
- `ontologies/sow/sow_inference_rules.owl` - SWRL inference rules
- `sparql_navigation_examples.json` - Lambda-ready SPARQL queries

### Development Standards
- Follow W3C Semantic Web standards (OWL, RDF, RDFS, SKOS)
- Maintain semantic completeness scores above 85%
- All classes must have rdfs:isDefinedBy properties
- Implement bidirectional navigation with owl:inverseOf
- Include concrete examples in SKOS annotations

### Cross-Repository Dependencies
- **Core Dependency**: None (foundation layer)
- **Used By**: All other repositories for semantic validation
- **Related**: `agentic-core-engine` for domain models

### Key Commands
```bash
# Semantic validation (requires RDFLib)
python -c "from rdflib import Graph; g = Graph(); g.parse('ontologies/bridge/gist_dbc_bridge.owl'); print(f'Loaded {len(g)} triples')"

# SPARQL endpoint testing
python -m sparql_server --ontology ontologies/
```

### Lambda Readiness
This repository provides semantic metadata for Lambda functions to discover and navigate concepts programmatically. Target: 90%+ semantic completeness for production deployment.