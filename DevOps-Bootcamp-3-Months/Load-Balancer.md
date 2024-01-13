# Load Balancer Google Cloud Guide: Understanding Architecture

## Introduction

This guide provides a overview of key concepts and pratical tips for **Load Balancer**.

## Architecture

![image](https://github.com/oCaioOliveira/Codex/assets/54439337/f8d47307-e35b-4bf8-9fff-e46a0aad30f8)

### Anycast IP

Anycast IP is a routing technique where multiple servers globally advertise the same IP address. When client initiates a request, the Anycast IP directs it to the nearest server node, optimizing response times. This approach minimizes latency, enhances availability by redistribuiting traffic among active nodes, and enables global scalability, ensuring a swift and reliable experience for users worldwide.

### Global Forwarding Rule

This rule determines how incoming traffic is distributed across the backend instances. When a request reaches the load balancer, the Global Forwarding Rule plays a pivotal role in determining how and where to forward that request, like a traffic cop, directing requests to the appropriate bakcend resources based on defined criteria.

### Target Proxy 

Target Proxy determines which backend service should handle the incoming request based on various factors, including session affinity, URL map configurations and health checks. In summary, serves as a central controller that influences how requests are routed from de frontend to the backend services.

### URL Map

The URL Map provide a mechanism to route incoming requests to the appropriate backend service based on URL paths.

### Health Check

Health Checks periodically assess the health and status of the instances to which traffic is being directed. If an instance fails a health check, the load balancer intelligently redirects traffic away from that unhealthy instance, preventing it from receiving requests until it is deemed heathy again.

## Version History

Name | Description | Version | Date |
---- | ----------- | ------- | ---- |
Caio | Create Load Balancer Guide | 1.0.0 | 13/01/2024 |
