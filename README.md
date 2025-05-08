# Neo4j RAG Workshop — May 2025

Welcome to the hands-on workshop for Retrieval-Augmented Generation (RAG) with Neo4j, OpenAI, and PDF/SEC data!

---

## 🚀 Workshop Goals
- Learn how to build a knowledge graph from real documents (10-Ks, CSVs)
- Practice loading, querying, and analyzing data in Neo4j AuraDB
- Explore retrieval-augmented generation (RAG) with OpenAI and LangChain


---

## 📂 Project Structure
- **PDF Loader Script for Neo4j GraphRAG.py** — Loads PDF content and structured data into Neo4j, builds the graph, and creates vector embeddings.
- **Retreivers_notebook.ipynb** — Interactive notebook for querying the graph, running RAG workflows, and debugging retrievals.
- **company_name_utils.py** — Utility for normalizing and filtering company names.
- **data/** — Sample CSVs and PDFs for ingestion.
- **.env.sample** — Template for required environment variables (never commit your real `.env`!).

---

## 🛠️ Setup Instructions
1. **Clone the repo**
2. **Install requirements**
   ```bash
   pip install -r requirements.txt
   ```
3. **Copy `.env.sample` to `.env` and fill in your credentials:**
   - `OPENAI_API_KEY` (never share or commit!)
   - `NEO4J_URI`, `NEO4J_USERNAME`, `NEO4J_PASSWORD`
4. **Start Neo4j AuraDB** (see workshop handout for connection details)
5. **Run the loader script** to ingest data
6. **Open the notebook** to run retrievals and explore the graph

---

## 🧑‍💻 Workshop Activities
- Load and normalize company data from CSV
- Ingest PDF filings, extract entities/relationships
- Connect risk factors to documents in the graph
- Use Neo4j Data Impor in the console to load data
- Run natural language and Cypher-powered retrievals
- Visualize and analyze graph results

---

## 📝 Best Practices
- **Never commit secrets** — `.env` is in `.gitignore` by default
- Use `requirements.txt` for reproducible environments
- Modularize code for easy experimentation
- Use the notebook for interactive exploration and debugging

---

## 🏃‍♂️ Running the Agent in the Notebook

Open `Retreivers_notebook.ipynb` in Jupyter or VS Code. Look for the section titled **"Conversational Agent"** or similar.

- Run the setup cells to load environment variables and initialize the agent.
- Use the provided code cell to ask questions, for example:
  ```python
  agent.ask("What are the risk factors for Apple?")
  agent.ask("Show all companies facing cybersecurity threats.")
  ```
- The agent will use Neo4j and OpenAI to answer using your loaded graph data.

> **Tip:** You can modify the notebook to experiment with custom queries or workflows!

---

## 📚 Resources
- [Neo4j AuraDB](https://console.neo4j.io/)
- [OpenAI API](https://platform.openai.com/)
- [LangChain Docs](https://python.langchain.com/docs/)
- [Neo4j Python Driver](https://neo4j.com/docs/api/python-driver/current/)

---

**Enjoy the workshop!**

For help, ask an instructor or open an issue in this repo.
