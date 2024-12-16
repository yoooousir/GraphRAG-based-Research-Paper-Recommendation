# 연구 논문 자동화 처리 및 GraphRAG 통합 프레임워크

## 📜 프로젝트 개요
사용자 정의 검색 쿼리 또는 키워드를 기반으로 연구 논문을 자동으로 검색, 파싱, 저장하는 프레임워크를 설계하고 구현한 프로젝트입니다. PUBMED 및 EuropePMC API를 통해 논문 데이터를 수집하고, PDF 및 XML 파일을 파싱한 결과를 Parquet 형식으로 변환하여 Azure Blob Storage에 저장합니다.

저장된 데이터는 GraphRAG 시스템과 통합되어, **논문에서 추출한 taxon, gene, link_keyword 간의 관계를 그래프로 구성**합니다. 사용자의 입력에 따라 가장 관련성이 높은 노드를 따라 탐색하며, 최종적으로 가장 적합한 답변을 제공합니다. 이 시스템은 LangChain 프레임워크와 Neo4j 데이터베이스를 기반으로 구축되었으며, Cypher 쿼리를 활용해 효율적으로 그래프를 탐색합니다.

---

## 📂 주요 기능
1. **연구 논문 자동화 처리**
   - PUBMED 및 EuropePMC API를 활용하여 논문 데이터 수집.
   - PDF 및 XML 파일 다운로드 및 파싱.
   - Parquet 형식으로 변환하여 Azure Blob Storage에 저장.

2. **GraphRAG 기반 검색**
   - 논문에서 추출한 **taxon, gene, link_keyword** 정보를 그래프 노드로 구성.
   - Neo4j를 활용해 데이터를 저장하고 Cypher 쿼리로 탐색.
   - 사용자의 질문에 따라 가장 관련성이 높은 노드와 엣지를 따라가며 적합한 정보를 반환.

3. **데이터 시각화**
   - GraphRAG 데이터 구조를 시각화하여 노드 간의 연관성을 직관적으로 분석.

---

## 🛠 기술 스택
- **언어 및 프레임워크**: Python, LangChain
- **데이터베이스**: Neo4j
- **API**: PUBMED, EuropePMC
- **클라우드**: Azure Blob Storage
- **파일 형식**: Parquet
- **쿼리 언어**: Cypher

---

## 📑 파일 구조
- `Azure_GraphRAG(Neo4j).ipynb`: LangChain GraphRAG 예제 실행 및 Neo4j와의 통합 코드.
- `GraphRAG__with_research_article_parquet_files.ipynb`: Azure Blob Storage에서 가져온 parquet 파일을 기반한 GraphRAG 실행 및 시각화 코드.
- `PUBMED_API_query_based_article_download.ipynb`: PUBMED 및 EuropePMC API를 활용한 논문 크롤링 코드.

---
