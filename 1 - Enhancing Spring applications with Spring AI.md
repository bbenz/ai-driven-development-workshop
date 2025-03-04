# Part 1 - Enhancing Spring applications with Spring AI
## Workshop: AI-Driven Development: Enhancing Java with the latest AI Innovations

## Introduction to AI Development with Spring Boot

This part of the workshop guides experienced Java developers through enhancing Spring Boot applications with AI capabilities using Spring AI, focusing on integration with Azure OpenAI services. You'll learn how to implement various AI patterns including basic prompting, RAG (Retrieval Augmented Generation), and more.

## Prerequisites

- Java 17 or later
- Maven
- Git
- Azure account with access to Azure OpenAI Service
- Basic Spring Boot knowledge

## Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Azure-Samples/spring-ai-azure-workshop
cd spring-ai-azure-workshop
```

### 2. Azure OpenAI Service Configuration

1. Create an Azure OpenAI Service instance in the Azure portal
2. Create two model deployments:
   - `gpt-35-turbo-16k` (for chat completions)
   - `text-embedding-ada-002` (for embeddings)
3. Locate your service credentials:
   - Navigate to: Azure Portal > Resource Group > OpenAI Service > Keys and Endpoint
   - Copy the endpoint URL and one of the keys

### 3. Configure Environment Variables

**For Linux/macOS:**
```bash
export SPRING_AI_AZURE_OPENAI_ENDPOINT=https://your-resource-name.openai.azure.com/
export SPRING_AI_AZURE_OPENAI_API_KEY=your-api-key
```

**For Windows:**
```cmd
set SPRING_AI_AZURE_OPENAI_ENDPOINT=https://your-resource-name.openai.azure.com/
set SPRING_AI_AZURE_OPENAI_API_KEY=your-api-key
```

### 4. Configure Application Properties

Ensure your `application.properties` file includes:

```properties
spring.ai.azure.openai.chat.options.model=gpt-35-turbo-16k
spring.ai.azure.openai.embedding.options.model=text-embedding-ada-002
```

## Workshop Exercises

### Exercise 1: Simple AI Integration - "Hello World"

Build and run the application:

```bash
./mvnw clean package
./mvnw spring-boot:run
```

Test your first AI endpoint by visiting:
```
http://localhost:8080/ai/simple
```

This demonstrates basic AI integration by asking the model to tell a joke.

### Exercise 2: Parameterized Prompts

Test sending parameters to influence the AI response:

```bash
curl --get --data-urlencode 'adjective=funny' --data-urlencode 'topic=cow' http://localhost:8080/ai/prompt
```

Examine how the controller passes these parameters to the AI model using a templated prompt.

### Exercise 3: Structured Output

Default response (about Jeff Bridges):
```bash
curl http://localhost:8080/ai/output
```

Customized response (changing the actor):
```bash
curl --get --data-urlencode 'actor=Bill Murray' http://localhost:8080/ai/output
```

Observe how the application uses output parsers to convert AI responses to structured Java objects.

### Exercise 4: Retrieval Augmented Generation (RAG)

Visit:
```
http://localhost:8080/ai/rag
```

Watch the terminal output carefully to understand the RAG workflow:
1. Loading documents
2. Converting documents to embeddings
3. Storing embeddings in a vector database
4. Retrieving relevant content based on similarity to the query
5. Using retrieved content to augment the prompt to the LLM

The complete RAG implementation details can be found at:
[RAG Implementation Guide](https://github.com/bbenz/spring-ai-azure-workshop/blob/main/6-README-retrieval-augmented-generation.md)

## Key Concepts

- **Spring AI**: Spring's integration framework for AI services
- **Prompt Engineering**: Techniques for effectively communicating with AI models
- **Azure OpenAI Integration**: Configuring and using Azure's OpenAI services
- **Output Parsing**: Converting AI responses to structured data
- **RAG (Retrieval Augmented Generation)**: Enhancing AI responses with relevant document context

## Advanced Topics

- Implementing memory in conversational interfaces
- Fine-tuning models for specific domains
- Securing AI endpoints and managing API keys
- Rate limiting and cost management
- Evaluating AI response quality

## Additional Resources

- [Spring AI Documentation](https://docs.spring.io/spring-ai/reference/)
- [Azure OpenAI Service Documentation](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [LangChain4j Documentation](https://docs.langchain4j.dev/)
- [GitHub Copilot](https://github.com/features/copilot)

## Troubleshooting

- Ensure environment variables are set correctly in each terminal window
- Check Azure OpenAI Service quotas and limits
- Verify model deployments are complete and active
- Review application logs for specific error messages