---
author: Andrey Tagarev - Ontotext
title: "How to Design a Successful SemTech PoC"
format: revealjs
metadata-files:
- ../_metadata.yml
---

# Typical Use Case

## Steps in Typical Use Case

What is a typical use case for a PoC?

. . . 

* Start with a question we want answered
* Have some data that partially answers the question

. . .

* Piece of the picture is missing but we can find it in LOD

. . .

* Create abstract model presenting the ideal data

. . .

* Transform sources from tabular to graphical form (ETL)

. . .

* Merge sources into a single dataset

. . .

* Further transformation to match data to our ideal data model

. . .

* Use finalized dataset to get answers 

# Our Use Case

## Our Use Case

### **Nepotism in Hollywood**

. . . 

**nepotism** /ˈnɛpətɪz(ə)m/

The practice among those with power or influence of favouring relatives or friends, especially by giving them jobs.


. . .

Mid 17th century: from French népotisme, from Italian nepotismo, from nipote ‘nephew’ (with reference to privileges bestowed on the ‘nephews’ of popes, who were in many cases their illegitimate sons).


## Simplified IMDB dataset

Our dataset is a simplified version of the public IMDB dataset

![](img/sources-imdb-table.png)

## Sources for Semantic Integration: LOD Cloud

* <a href=https://lod-cloud.net>https://lod-cloud.net</a>

![](img/sources-lod-cloud.png)

## Sources for Semantic Integration: Datahub

* <a href=https://datahub.io>https://datahub.io</a>

![](img/sources-datahub.png)

## Sources for Semantic Integration: Google Dataset Search

![](img/GoogleDatasetSearch.png)

## Sources for Semantic Integration: Google Cloud Public Datasets

![](img/GoogleCloudDatasetSearch.png)

## Sources for semantic Integration: DBPedia

* <a href=https://wiki.dbpedia.org>https://wiki.dbpedia.org</a>

![](img/sources-dbpedia.png)

# Analysis

## Analyse and document peculiarities of source data

. . . 

* number of records

. . .

* coverage of features (i.e. how many missing features)

. . .

* range of numeric features

. . .

* range of date features

. . .

* repetitive values in text features

# Auxiliary Resources

## Select existing auxiliary resources relevant to use case

. . .

* FOAF (Friend of a Friend)

. . .

* OWL

. . .

* Movie Ontology (not needed for this POC)

. . .

* Others to consider 

# Perform semantic conversion (ETL procedure)

## ETL Basics

ETL is short for extract, transform, load:

* **Extract**: the process of collecting the data, often from multiple and different types of sources.
* **Transform**: the process of *converting* the extracted data into the RDF so that it can be placed into GraphDB
* **Load**: the process of writing the data into GraphDB

. . .

In short, how do we turn multiple datasets of different formats into **a single RDF dataset**.

## Normalise values

OntoRefine _text facets_ allow quick bulk-editing of values 

![](img/OR-normalize.png)

`United States` is normalised to `USA` in 122 cells 

## Create new columns 

Split columns according to a separator character 

![](img/OR-columns-in.png)

![](img/OR-columns-out.png)

## Urlify 

Edit the text in the cells

![](img/OR-urlify.png)

Remove whitespace so that the string can be used in a 
url/iri 

## Reconcile 

Use a reconciliation service to match strings to real world objects. 

`Bulgaria` > `https://www.wikidata.org/wiki/Q219`  

## Tabular to Linked Data

Moving from tabular data to linked data

![](img/OR-table-to-graph.png)

## Tabular to Linked Data

Here is what our cleaned up table looks like...

![](img/OR-rdf-table.png)

## Tabular to Linked Data

... but here it is transformed into RDF.

![](img/OR-rdf-graph.png)

# Data Integration

## Initial data model

Output from our ETL procedure

![](img/Model-stage-1.png)

. . .

Does this model contain all the data we need?

## Expanding the initial model

Incorporating data from an additional data source.

![](img/Model-stage-2.png)

. . .

Can we simplify things?

## Creating a new property

Single symmetric relation to use in a straightforward manner.

![](img/Model-stage-3.png)

. . .

Can we simplify things further?

## Creating a second new property

Three relations transformed into a single one.

![](img/Model-stage-4.png)

. . .

But we are still working with two disconnected parts.

## Connecting the dataset

Now we have everything we need to ask our question.

![](img/Model-stage-5.png)

. . .

What if we want to ask a more complex question?

## Changing the model

At later stages we can rework the model which will then require corresponding changes to the procedure.

![](img/Model-stage-6.png)

# Ontotext GraphDB Visualization 

## Google charts

Visualize data in google charts in GDB 

![](img/VIS-countries.png)

## Visual graph 

Highly configurable network visualisation using `SPARQL`

![](img/OR-rdf-graph.png)

## Visualize family Relations 

![](img/VIS-relatives.png)

## Visualize family Relations 2

![](img/VIS-relatives-closeup.png){height=700px}

## Is there nepotism in Holywood?

![](img/VIS-nepotism.png){height=700px}

## Building a Semantic POC - Conclusion 

1. Start with a question we want answered
1. Have some data that partially answers the question
1. Piece of the picture is missing but we can find it in LOD
1. Create abstract model presenting the ideal data
1. Transform sources from tabular to graphical form (ETL)
1. Merge sources into a single dataset
1. Further transformation to match data to our ideal data model








 
