---
author: Vladimir Alexiev, PhD, PMP
title: "Ontotext CH/DH Projects"
subtitle : "Knowledge Graphs and Semantic Integration. TimeMachine meeting, Nuremberg"
date: "2018-06-01"
format: revealjs
metadata-files:
  - ../_metadata.yml
---

## About [Ontotext](http://ontotext.com)

- Founded 2000, part of [Sirma Group](https://sirma.com/) (400 people, [BSE:SKK](http://www.bse-sofia.bg/?page=QuotesInfo&type=S&code=SKK&compnum=350), part of SOFIX), venture funding 2008
- 65 people: 7 PhD, 30 MS, 20 BS, 6 university lecturers. Offices in Sofia, Varna, London
- Core part of [Sirma Strategy 2022](https://2022.sirma.com/en/) with focus on cognitive computing
- Working on: semantic technologies, semantic text analysis and machine learning
- Semantic Graph Database: [Ontotext GraphDB](http://graphdb.ontotext.com)
- Semantic data integration and building Knowledge Graphs
- Semantic text analysis: entity, concept, relation extraction, document classification
- Recommendations, sentiment analysis
- Machine learning: entity disambiguation, deep learning in graphs, etc

## Research Projects

![](https://github.com/VladimirAlexiev/VladimirAlexiev.github.io/raw/master/Ontotext-FP-projects-timeline.png){height=550px}

## Industries and Clients
- 80% of our sales are in the UK and US 
- Media: BBC, UK Press Association, NL Press Association (NDP)
- Financial Info: S&P Global Platts, Euromoney, Financial Times, Nikkei
- STEM Publishing: IET, Oxford University Press, Wiley, Elsevier, Springer Nature
- Life Science: AstraZeneca, Novartis
- Government: UK Parliament, The National Archives, Natural Resources Canada
- Cultural Heritage and Digital Humanities (see next)

## CH/DH Projects
- ResearchSpace: British Museum, Yale Center for British Art. Largest museum collection, CIDOC CRM, semantic search...
- (with Sirma Enterprise) [ConservationSpace](http://conspace.wixsite.com/conservationspace), [Sirma MuseumSpace](https://museumspace.com/)
- [Medieval Cultures and Technological Resources](http://www.cost.eu/COST_Actions/isch/IS1005) (VCMS) COST action
- Europeana: [Creative](https://pro.europeana.eu/project/europeana-creative-project), [Food and Drink](https://foodanddrinkeurope.eu/) ([sem app](http://efd.ontotext.com/app)), [OAI PMH](http://oai.europeana.eu/oaicat/index.shtml), [SPARQL](https://pro.europeana.eu/resources/apis/sparql), [members council](https://pro.europeana.eu/post/meet-the-members-council-vladimir-alexiev), 5 work groups, [Data Quality Committee](https://pro.europeana.eu/project/data-quality-committee)
- [Bulgariana](http://bulgariana.eu) national aggegator, CLADA (BG CLARIN+DARIAH)
- [Getty Research Institute: vocabularies LOD](http://vocab.getty.edu)
- [Carnegie Hall LOD](https://github.com/CarnegieHall/linked-data)
- [American Art Collaborative](http://americanartcollaborative.org/) consulting: 14 US museums integrating data using CIDOC CRM
- [European Holocaust Research Infrastructure](https://ehri-project.eu): semantic archive integration. 4+4 years, heading towards ERIC
- [Canadian Heritage Information Network](https://www.canada.ca/en/heritage-information-network.html) consulting (national aggregator moving to LOD)
- Wikidata: frequent contributions (authority control)
- DBpedia: contributions, association member, data quality and ontology committee

## Semantic Data Integration (1)
- Well-developed [process](https://docs.google.com/document/d/18LkRMBp8ipQmy16SJQk-M2L3xP7oA4ZyqtdepND3mN4/edit)
- Business case, competence questions
- Dataset analysis and understanding
  - Knowledge and exploration of useful external datasets (leverage LOD)
- Semantic Modeling
  - Selection of existing ontologies
  - Engineering of new ontologies (ontology creation methodologies, ontology design patterns, naming conventions)
  - RDF profile/shape development (also key for validation
  - URL (IRI) strategies and design

## Semantic Data Integration (2)
- Model documentation
  - Diagrams
  - Detailed ontology term description, Examples
  - Data provider rules
  - Sample queries
- Semantic conversion/ETL/ingestion
  - Tool selection: OntoRefine, Karma, R2RML, rdfpuml/rdf2rml, TARQL, XSPARQL, LIXR...
  - Maintainability, Reproducibility/portability, Data cleansing

## Semantic Data Integration (3)
- Semantic data enrichment
  - Inference. Attributes and relations are added based on rules. 
  - Thesaurus harmonisation
  - Entity and relation extraction
  - Link discovery (eg graph based ML)
  - Instance matching (clustering, linking, deduplication)
  - Data fusion (redundant/conflicting data is deduplicated/fused)
- Quality Assurance
  - Data is validated with respect to model
  - Deploy RDF shapes tools (SHACL or ShEx)
  - Data quality tracking (issue tracking system for data)

## Semantic Data Integration (4)
- Data Update flows
  - Detecting updates (push, pull/requery, update timestamps)
  - Update impact anlaysis (eg on instance clusters, derived data)
  - Implementing incremental updates (GraphDB smooth delete)
  - Data aggregation issues (volume)
- Semantic publishing and consumption
  - Semantic publishing of: model, nomenclatures, instance data
  - Proper semantic resolution and Content negotiation (HTML and various RDF formats)
  - Services such as SPARQL querying, autocomplete
  - Data service availability monitoring 

## Knowledge Graphs

| Knowledge Graph |   Year   | M obj | B triples |
|---------------- |:--------:|:-----:|:---------:|
| British Museum  |   2013   |   2   |    0.92   |
| Polish DL       |   2013   |  3.1  |    0.53   |
| Europeana       |   2014   |  20.3 |    3.8    |
| FactForge       | 2006-now |  ~14  |    3.2    |
| LinkedLifeData  | 2008-now |  ~12  |    10.2   |
| Company Graph   | 2017-now |   6   |    3      |
| Dun & Bradstreet|   2017   |  210  |    30     |

Details about the first 5 are in V.Alexiev et al, [Large-scale Reasoning with a Complex Cultural Heritage Ontology (CIDOC CRM)](http://vladimiralexiev.github.io/pubs/Alexiev2013-CRM-reasoning-slides.ppt), Workshop Practical Experiences with CIDOC CRM and its Extensions (CRMEX), TPDL 2013, slide 17
