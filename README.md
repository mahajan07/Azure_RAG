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
```

# 🔐 2. Add Your API Keys (.env)
**Create a .env file in your project root. Add your Azure OpenAI and Search credentials:**
```bash
# Azure OpenAI
OPENAI_API_TYPE="azure"
OPENAI_API_BASE="https://your-resource.openai.azure.com/"
OPENAI_API_KEY="your_openai_key"
OPENAI_API_VERSION="2023-07-01-preview"

# Azure Cognitive Search
SEARCH_SERVICE_NAME="your-search-url"
SEARCH_API_KEY="your_search_key"
SEARCH_INDEX_NAME="your-index-name"
```


# 📈 3. Preprocess & Sample Data
**If your CSV is large, sample 100 rows and clean the data for embeddings:**
```bash
import pandas as pd

df = pd.read_csv('data/your_file.csv')
df_sample = df.sample(n=100, random_state=42).dropna(axis=1, how='all')
records = df_sample.to_dict('records')
```

# 🐳 4. Azure Container App Deployment (Optional)
1. Use at least 2 CPU cores and 4GB RAM
2. Expose port 80
3. Use a GitHub PAT for ghcr.io registry access

# 🧾 Create a Service Principal
```bash

az ad sp create-for-rbac --name "CICD" --role contributor \
  --scopes /subscriptions/$AZURE_SUBSCRIPTION_ID --sdk-auth
```
# 🧪 Testing the Pipeline
This project includes examples for:

✅ Creating text embeddings from structured data
✅ Retrieving relevant content using vector similarity
✅ Generating grounded responses with LLMs

You can run the demo script or build a custom FastAPI wrapper.














