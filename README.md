# The-Coffee-Shop
### The-Coffee-Shop Microservices

This repository contains a set of microservices that simulate a coffee shop, with added observability using OpenTelemetry and Jaeger. The microservices include:

- **order-service**: responsible for managing orders and communicating with payment-service and inventory-service to handle payments and update inventory data.
- **payment-service**: handles payments and communicates with order-service to report payment status.
- **inventory-service**: manages inventory data and communicates with order-service to update inventory information.
- **barista-service**: consumes messages from order-service through Kafka and prepares coffee, then reports back to order-service to complete the order cycle.

All services are written in Java using Spring Boot 2.7.7 and communication between services is done through gRPC and Kafka. Data is persisted in a MongoDB collection and all services including OpenTelemetry, Jaeger, MongoDB are deployed with Docker.
