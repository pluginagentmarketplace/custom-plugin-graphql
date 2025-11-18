---
name: ai-ml-engineering
description: Build AI-powered applications using LLMs, prompt engineering, and AI agents. Use when working with ChatGPT, Claude, LLM APIs, RAG systems, or AI applications.
---

# AI/ML Engineering & LLMs

## Quick Start

AI is transforming how we build applications. Get started with LLMs:

### LLM Basics

```python
# Using OpenAI API
from openai import OpenAI

client = OpenAI(api_key="your-api-key")

response = client.chat.completions.create(
    model="gpt-4",
    messages=[
        {"role": "system", "content": "You are a helpful assistant."},
        {"role": "user", "content": "What is Python?"}
    ]
)

print(response.choices[0].message.content)
```

### Prompt Engineering

```python
# Bad prompt
"What is Python?"

# Good prompt (specific, context, instructions)
"""You are an experienced software engineer.
Explain Python in simple terms suitable for beginners.
Include 2-3 practical examples.
Keep response under 200 words."""

# Few-shot prompting (examples)
"""Classify sentiment of tweets.

Examples:
Tweet: "I love this product!" → Positive
Tweet: "Worst experience ever" → Negative

Tweet: "It works fine"
Sentiment:"""

# Chain-of-thought (step-by-step reasoning)
"""Solve step by step:
1. Understand the problem
2. Break into sub-problems
3. Solve each part
4. Combine solutions"""
```

### Building with LangChain

```python
from langchain.chat_models import ChatOpenAI
from langchain.prompts import ChatPromptTemplate
from langchain.chains import LLMChain

# Create prompt template
prompt = ChatPromptTemplate.from_template(
    "Explain {topic} in simple terms"
)

# Create LLM chain
llm = ChatOpenAI(model="gpt-4")
chain = LLMChain(prompt=prompt, llm=llm)

# Use chain
result = chain.run(topic="Machine Learning")
print(result)
```

### RAG (Retrieval-Augmented Generation)

```python
from langchain.embeddings import OpenAIEmbeddings
from langchain.vectorstores import Pinecone
from langchain.chains import RetrievalQA

# 1. Load documents
documents = load_documents("company_docs/")

# 2. Create embeddings
embeddings = OpenAIEmbeddings()

# 3. Store in vector database
vector_db = Pinecone.from_documents(
    documents,
    embeddings,
    index_name="company-docs"
)

# 4. Create QA chain
qa = RetrievalQA.from_chain_type(
    llm=llm,
    retriever=vector_db.as_retriever(),
    chain_type="stuff"
)

# 5. Answer questions using your docs
answer = qa.run("What is our company policy on remote work?")
```

### AI Agents

```python
from langchain.agents import initialize_agent, Tool
from langchain.agents import AgentType

# Define tools
tools = [
    Tool(
        name="Calculator",
        func=calculator.run,
        description="Useful for math"
    ),
    Tool(
        name="Search",
        func=search.run,
        description="Search the web"
    )
]

# Create agent
agent = initialize_agent(
    tools,
    llm,
    agent=AgentType.ZERO_SHOT_REACT_DESCRIPTION,
    verbose=True
)

# Use agent
agent.run("What is 2+2 and show me weather in NYC?")
```

## Key Concepts

- **Tokens**: Words/subwords LLMs process
- **Context Window**: Max tokens model can handle
- **Temperature**: Randomness in responses (0=deterministic, 1=creative)
- **Top-p**: Diversity control
- **Embedding**: Vector representation of text
- **Vector Database**: Store and search embeddings

## LLM Models

```
Proprietary:
- OpenAI: GPT-4, GPT-3.5-turbo
- Anthropic: Claude, Claude Instant
- Google: PaLM, Gemini
- Cohere: Command, Embed

Open Source:
- Llama 2 (Meta)
- Mistral
- MPT
- OpenLLaMA
```

## Vector Databases

```
Popular options:
- Pinecone: Cloud managed
- Weaviate: Open source, self-hosted
- Milvus: Open source, scalable
- Qdrant: Rust-based, high performance
- FAISS: Facebook's search library
```

## Application Patterns

- **Chatbots**: Conversational AI
- **RAG Systems**: Q&A with documents
- **Agents**: Autonomous task execution
- **Content Generation**: Writing, coding
- **Classification**: Categorizing text
- **Summarization**: Condensing content

## Learning Path

1. Learn LLM fundamentals and limitations
2. Master prompt engineering techniques
3. Build simple chatbots
4. Implement RAG systems
5. Create AI agents with tools
6. Deploy applications
7. Handle errors and edge cases
8. Implement feedback loops

## Best Practices

```python
# Cost optimization
- Use cheaper models (gpt-3.5-turbo vs gpt-4)
- Implement caching
- Batch requests

# Quality
- Use system prompts for consistency
- Validate outputs
- Implement error handling

# Safety
- Monitor for hallucinations
- Implement input validation
- Set rate limits
- Log for audit trail
```

## Resources

- **OpenAI**: platform.openai.com
- **Anthropic**: claude.ai
- **LangChain**: langchain.com
- **LlamaIndex**: llamaindex.ai
- **Hugging Face**: huggingface.co
