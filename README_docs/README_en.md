# Automated Research Article Processing and GraphRAG Integration Framework

## 📜 Project Overview
This project involves designing and implementing a framework to automate the retrieval, parsing, and storage of research articles based on user-defined search queries or keywords. The framework leverages the PUBMED and EuropePMC APIs to fetch research article data, parses PDF and XML files, and stores the processed data as Parquet files in Azure Blob Storage.

The processed data is integrated into a GraphRAG system that constructs relationships between **taxon, gene, and link_keyword** as a graph. Based on user input, the system traverses the most relevant nodes and edges to return the most appropriate answers. This system is built on the LangChain framework and Neo4j database, utilizing Cypher queries for efficient graph traversal.

---

## 📂 Key Features
1. **Automated Research Article Processing**
   - Collects research article data using PUBMED and EuropePMC APIs.
   - Downloads and parses PDF and XML files.
   - Converts parsed data into Parquet format and stores it in Azure Blob Storage.

2. **GraphRAG-Based Retrieval**
   - Constructs graph nodes using **taxon, gene, and link_keyword** information extracted from research articles.
   - Stores and queries data using Neo4j and Cypher queries.
   - Traverses relevant nodes and edges based on user queries to return accurate information.

3. **Data Visualization**
   - Visualizes the GraphRAG data structure for intuitive analysis of relationships between nodes.

---

## 🛠 Tech Stack
- **Languages & Frameworks**: Python, LangChain
- **Database**: Neo4j
- **APIs**: PUBMED, EuropePMC
- **Cloud**: Azure Blob Storage
- **File Format**: Parquet
- **Query Language**: Cypher

---

## 📑 File Structure
- `Azure_GraphRAG(Neo4j).ipynb`: Example code for running LangChain GraphRAG and integrating with Neo4j.
- `GraphRAG__with_research_article_parquet_files.ipynb`: GraphRAG execution and visualization using Parquet files retrieved from Azure Blob Storage.
- `PUBMED_API_query_based_article_download.ipynb`: Code for crawling research articles using PUBMED and EuropePMC APIs.

---
