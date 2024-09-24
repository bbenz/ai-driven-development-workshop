# Start up the Spring Boot application
./mvnw spring-boot:run

# First demo - Tell me a joke (hello world)
http://localhost:8080/ai/simple

# Second demo 
# Open a new Ubuntu Window
curl --get  --data-urlencode 'adjective=funny' --data-urlencode 'topic=cow' http://localhost:8080/ai/prompt 

# Fourth demo 
# Open a new Ubuntu Window
# Defaul - Jeff Bridges
curl http://localhost:8080/ai/output
# Prompted
curl --get  --data-urlencode 'actor=Bill Murray' http://localhost:8080/ai/output 



