 # AMQP Message Sender

 This project is a Spring Boot application for sending messages using AMQP (Advanced Message Queuing Protocol) with RabbitMQ. It provides a REST API to send messages and is designed for educational and demonstration purposes.

 ## Features
 - Send messages to RabbitMQ queues
 - RESTful API endpoints
 - Configurable via `application.yml`
 - Docker Compose support for local development

 ## Technologies Used
 - Java 17+
 - Spring Boot
 - Spring AMQP
 - RabbitMQ
 - Docker Compose

 ## Getting Started

 ### Prerequisites
 - Java 17 or higher
 - Maven
 - Docker & Docker Compose

 ### Build and Run

 1. **Clone the repository**
    
 2. **Start RabbitMQ with Docker Compose**
    ```sh
    docker-compose up -d
    ```

 3. **Build the application**
    ```sh
    mvn clean package
    ```

 4. **Run the application**
    ```sh
    mvn spring-boot:run
    ```

 ### API Usage
 - **POST /api/messages**
   - Send a message to the queue.
   - Example request body:
     ```json
     {
       "content": "Hello, RabbitMQ!",
       "sender": "user1"
     }
     ```

 ## Configuration
 - Edit `src/main/resources/application.yml` to change RabbitMQ or application settings.

 ## Project Structure
 - `amqp-message-sender/` - Main Spring Boot application
 - `docker-compose.yml` - Docker Compose file for RabbitMQ

 ## License
 This project is licensed for educational use.
