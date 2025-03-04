# Workshop: AI-Driven Development: Enhancing Java with the latest AI Innovations
# Afternoon: **Building Intelligent Java Applications with Langchain4j**

### **Workshop Duration: 3-4 hours**

---

## Introduction

This afternoon, we'll work with a practical demo using LangChain4j, a powerful framework for creating AI-powered applications in Java. We'll explore both GitHub-hosted AI models and local model options, learning about vector databases, embeddings, and retrieval-augmented generation (RAG).

## Prerequisites

- Basic Java and Spring Boot knowledge
- Docker Desktop installed
- Git installed
- GitHub account
- IDE (VS Code, IntelliJ IDEA, etc.)
- Maven (or we'll use the Maven wrapper)

## Workshop Outline

1. Environment Setup
2. Understanding the Architecture
3. Working with GitHub-hosted AI Models
4. Building a RAG System with Qdrant
5. Local LLM Deployment (Optional, if time permits)
6. Extending the Application

## 1. Environment Setup

### Docker Setup

```
# Start Docker Desktop
# Ensure it's running before proceeding
```

### Clone the Repository

```bash
git clone https://github.com/jdubois/jdubois-langchain4j-demo
cd jdubois-langchain4j-demo
```

### GitHub Token Setup

The AI functionality we'll use requires authentication with GitHub's API:

1. Go to https://github.com/settings/tokens
2. Click "Generate New Token" > "Classic"
3. Give your token a name (e.g., "LangChain4j Workshop")
4. Leave scopes/dfault/open/blank 
5. Click "Generate token"
6. **IMPORTANT**: Copy your token immediately as it won't be shown again!

> For detailed instructions on generating tokens, see: https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens

### Configure Application Properties

Edit application.properties to use GitHub models:

```properties
spring.profiles.active=github
```

### Set Environment Variable

For Linux/macOS/WSL:
```bash
export GITHUB_TOKEN=your_token_here
```

For Windows Command Prompt:
```cmd
set GITHUB_TOKEN=your_token_here
```

> **Note**: Replace `your_token_here` with the actual token you generated. The environment variable must be set in the same terminal session where you'll run the application.

## 2. Understanding the Architecture

Before diving into the code, let's understand what we're building:

- **LangChain4j**: A Java framework for building LLM applications
- **Vector Database (Qdrant)**: Stores and retrieves document embeddings
- **Embedding Models**: Convert text to numerical vectors to enable semantic search
- **LLM Models**: Generate responses based on prompts and context
- **RAG Pattern**: Retrieval-Augmented Generation combines search and generation

Our architecture will connect these components in a Spring Boot application.

## 3. Working with GitHub-hosted AI Models

### Set Up AI Models

Access models through GitHub Marketplace:
https://github.com/marketplace?type=models

For this workshop, we'll use:
- **Chat Model**: GPT-4o-mini via Azure OpenAI integration
  - https://github.com/marketplace/models/azure-openai/gpt-4o-mini
- **Embedding Model**: text-embedding-3-small
  - For semantic search capabilities

### Start the Infrastructure

```bash
# Navigate to Docker config directory
cd src/main/docker

# Start required services
docker-compose -f docker-compose-github.yml up
```

This launches:
- **Qdrant**: Vector database for storing embeddings
- **UI Access**: 
  - Qdrant dashboard at http://localhost:6333/dashboard

### Run the Application

Open a new terminal window (keeping the docker-compose terminal running):

```bash
# Set GitHub token in this terminal as well
export GITHUB_TOKEN=your_token_here  # (Linux/macOS/WSL)
# OR
set GITHUB_TOKEN=your_token_here  # (Windows)

# Navigate to project root and start the app
# The -Dmaven.test.skip=true flag skips tests for faster startup
# (You can run tests later if needed)

cd /path/to/jdubois-langchain4j-demo
./mvnw clean package -Dmaven.test.skip=true # (Linux/macOS/WSL)
./mvnw spring-boot:run  # (Linux/macOS/WSL)
# OR
mvnw clean package -Dmaven.test.skip=true # (Windows)
mvnw spring-boot:run  # (Windows)
```

Access the application at http://localhost:8080/

## 4. Building a RAG System with Qdrant

Let's explore what makes RAG powerful:

1. **Document Ingestion**: The demo already includes code to ingest documents
2. **Vector Embedding**: Documents are converted to embeddings using the text-embedding-3-small model
3. **Semantic Search**: Query embeddings are compared to document embeddings
4. **Contextual Response**: LLM generates responses based on retrieved content

Explore the codebase to understand:
- How documents are embedded and stored
- How queries retrieve relevant context
- How the LLM generates responses using this context

## 5. Local LLM Deployment (Optional)

If time permits, we can switch to local models:

### Update Application Properties

```properties
spring.profiles.active=local
```

### Start Local Infrastructure

```bash
cd src/main/docker
docker compose up
```

This will run:
- **Ollama**: Hosting Phi-3 and nomic-embed-text models
  - Web UI at http://localhost:8081/
- **Qdrant**: Vector database at http://localhost:6333/dashboard

### Run with Local Models

In a separate terminal:

```bash
cd /path/to/jdubois-langchain4j-demo
./mvnw clean package  # (Linux/macOS/WSL)

# OR 

mvnw clean package  # (Windows)
```

Then set the environment variable for local models:
```

Then run the application:

```bash
./mvnw spring-boot:run  # (Linux/macOS/WSL)
# OR
mvnw spring-boot:run  # (Windows)
```

## 6. Extending the Application

### Workshop Exercises

1. **Add New Document Sources**: Extend the application to ingest from different sources
2. **Customize the Prompts**: Modify the system prompts to change the AI's behavior
3. **Add Streaming Responses**: Update the UI to show streaming responses
4. **Implement Memory**: Add conversation memory to maintain context
5. **Benchmark Performance**: Compare response quality and latency between GitHub and local models

### Integration with GitHub Copilot

Explore how GitHub Copilot can help you:
- Generate boilerplate code for AI integration
- Debug issues with LLM integration
- Create prompts and system messages
- Implement proper error handling

### Azure AI Integration

For production environments, consider:
- Azure OpenAI Service for managed LLMs
- Azure AI Search for production-grade vector search
- Azure Container Apps for deployment
- Azure Key Vault for secure token storage

## Conclusion

By completing this portion of the workshop, you've workded with a modern AI application using Java and LangChain4j. You've learned about:

- Working with LLMs in Java applications
- Implementing the RAG pattern
- Using vector databases for semantic search
- Comparing cloud-hosted and local model deployment options

This is just the beginning of what's possible with AI and Java. We encourage you to continue exploring and building!

## Resources

- [LangChain4j Documentation](https://docs.langchain4j.dev/)
- [Qdrant Documentation](https://qdrant.tech/documentation/)
- [GitHub Copilot for Java Developers](https://github.blog/2023-03-22-github-copilot-for-java-developers/)
- [Azure AI Services](https://azure.microsoft.com/en-us/products/ai-services)

## Troubleshooting

Common issues:
- **Missing GITHUB_TOKEN**: Ensure the environment variable is set correctly
- **Docker Connectivity**: Verify Docker containers are running with `docker ps`
- **Port Conflicts**: Ensure ports 8080, 6333, and 8081 are available
- **Memory Issues**: Docker and JVM might need more memory for larger models

For assistance during the workshop, don't hesitate to ask your instructor!