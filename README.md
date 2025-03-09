# n8n Snowflake AI Workflow 🚀  
🔹 **Automated SQL Query Generation and Execution Using n8n, Snowflake, AWS S3, and AI**  

## 📌 Overview  
This project automates the process of querying **Snowflake** using **natural language**. It leverages **n8n**, **AWS S3**, and **LangChain AI** to generate and execute SQL queries dynamically.  

## 🛠 Tech Stack  
✅ **n8n** - No-code workflow automation  
✅ **Snowflake** - Cloud data warehouse  
✅ **AWS S3** - Schema storage  
✅ **LangChain AI Agent** - Converts natural language to SQL  

---

## 📌 Workflow Breakdown  

### 1️⃣ Schema Extraction Workflow (One-time Setup)  
Extracts schema from **Snowflake** and uploads it to **AWS S3**.  
- Lists all tables in the database.  
- Extracts schema metadata.  
- Converts it into a structured format and stores it in **S3**.  

### 2️⃣ Handling Messages & Schema Awareness  
Ensures the AI agent understands the database schema **without** direct access.  
- Downloads schema from **AWS S3**.  
- Converts it into **JSON format**.  
- Merges it with user queries before AI processing.  

### 3️⃣ AI-Powered SQL Generation  
Uses **LangChain AI** to translate user queries into SQL.  
- Ensures queries align with the schema.  
- Prevents AI hallucinations.  
- Passes only valid SQL forward.  

### 4️⃣ SQL Execution & Response Formatting  
Executes the AI-generated query in **Snowflake** and formats the response.  
- Checks if the query exists.  
- Runs the SQL query on **Snowflake**.  
- Formats the result and translates it into **natural language**.  

---

## 📌 Installation & Setup  

### 1️⃣ Clone the Repository  
```sh
git clone https://github.com/YOUR_GITHUB_USERNAME/n8n-snowflake-ai-workflow.git
cd n8n-snowflake-ai-workflow
