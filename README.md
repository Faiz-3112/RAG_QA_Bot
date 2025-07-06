# RAG_QA_Bot

A professional Retrieval-Augmented Generation (RAG) Question Answering Bot designed to answer business-related queries using advanced language models and vector search.

## Features
- **Business-Only QA**: Answers strictly business-related questions (operations, services, products, policies, pricing, support, transactions, hours, etc.).
- **Contextual Retrieval**: Uses Pinecone vector database and Sentence Transformers to retrieve relevant business document chunks.
- **Generative AI**: Integrates Google Gemini and OpenAI models for high-quality, context-aware responses.
- **Easy Setup**: Simple notebook-based workflow for rapid prototyping and deployment.

## Requirements
- Python 3.8+
- Jupyter Notebook or Google Colab
- API keys for:
  - OpenAI
  - Pinecone
  - Google Generative AI
- Required Python packages (auto-installed in the notebook):
  - openai
  - pinecone
  - google-generativeai
  - sentence-transformers

## Usage
1. **Clone or Download** this repository.
2. **Prepare your business document** as `business_doc.txt` (one or more paragraphs, separated by blank lines).
3. **Open `Task_1.ipynb`** in Jupyter or Colab.
4. **Insert your API keys** when prompted.
5. **Run all cells** to initialize the vector index and QA system.
6. **Ask your business-related questions** in the provided input cell.

## How it Works
- The notebook loads your business document, splits it into chunks, and embeds them using Sentence Transformers.
- Chunks are indexed in Pinecone for fast similarity search.
- When a user asks a question, the most relevant chunks are retrieved.
- The context is passed to a generative AI model (Gemini or OpenAI) to generate a precise, business-focused answer.
- Non-business or off-topic questions are politely declined.

## Example
```
Ask your business-related question: What are your support hours?
Answer: Our support hours are Monday to Friday, 9am to 6pm.
```

## Notes
- Only business-related queries are answered. Off-topic questions receive a polite refusal.
- Ensure your API keys are kept secure and not shared publicly.

## License
This project is strictly proprietary. Copying, redistributing, or using any part of this code or its contents without explicit written permission from the owner is strictly prohibited. For any use, distribution, or reference, you must obtain prior authorization. All rights reserved.
