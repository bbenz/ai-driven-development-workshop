# Log in to docker desktop
# Start Docker desktop

Clone https://github.com/bbenz/jdubois-langchain4j-demo

Follow the setup steps in the readme for docker setup

Check the local models 
An Ollama instance, with the Phi-3 and the nomic-embed-text models. Its Web UI is available at http://localhost:8081/.
A Qdrant instance. Its Web UI is available at http://localhost:6333/dashboard.

# Make sure that local execution is enabled by using the local Spring Boot profile - set spring.profiles.active=local in the src/main/resources/application.properties file.

cd C:\githublocal\jdubois-langchain4j-demo/src/main/docker

# Run the setup for local 
   docker compose up
   docker-compose up --pull always
   docker-compose down


# Check the local models 
# Ollama with Phi-3 and nomic-embed-text models - http://localhost:8081/.
# Qdrant - http://localhost:6333/dashboard

# Open a second command window - to run the demo
mvnw spring-boot:run

Open http://localhost:8080/
