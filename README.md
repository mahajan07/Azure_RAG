# 🚀 Retrieval Augmented Generation (RAG) with Azure – By Dewank Mahajan

A **production-ready RAG pipeline** built with:

- 🔍 **Azure Cognitive Search**
- 🤖 **Azure OpenAI**
- 📦 **Embeddings & FastAPI**
- 📊 **Sample CSV data grounding**

This project shows how to deploy scalable, secure, and extensible AI capabilities using Azure-native tools, empowering developers to build **custom LLM apps** grounded in enterprise data.

---

## 🛠️ Setup Instructions

### ✅ 1. Install Dependencies

Use the provided `requirements.txt` file to install all necessary packages:

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# 🔐 2. Add Your API Keys (.env)
**Create a .env file in your project root. Add your Azure OpenAI and Search credentials:**

# Azure OpenAI
OPENAI_API_TYPE="azure"
OPENAI_API_BASE="https://your-resource.openai.azure.com/"
OPENAI_API_KEY="your_openai_key"
OPENAI_API_VERSION="2023-07-01-preview"

# Azure Cognitive Search
SEARCH_SERVICE_NAME="your-search-url"
SEARCH_API_KEY="your_search_key"
SEARCH_INDEX_NAME="your-index-name"
