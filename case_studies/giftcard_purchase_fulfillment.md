# 📌 Gift Card Purchase & Fulfillment Flow

## Case Study Title
**Building a Scalable, Event-Driven Gift Card Fulfillment Platform**

---

## Context
- **Domain:** Retail E-Commerce  
- **Teams:** 3 cross-functional product & platform teams
- **Constraints:** Payment reliability, high transaction volume, customer experience, scalability  

---

## Project Overview

Led the design and delivery of a scalable, event-driven Gift Card Purchase and Fulfillment platform enabling customers to purchase, receive, and redeem digital gift cards seamlessly.
The solution integrated order management, payment processing, gift card issuance, and customer notifications while ensuring reliability, traceability, and a smooth end-user experience.

---

## Role

Technical Project Manager & Architect

---
## Key Workflow

### End-to-End Flow
 - Order Creation
  - Customer initiates gift card purchase
  - Order Service creates order in CREATED state
 - Payment Processing
  - Order Service invokes Payment Service
	- Payment Service authorizes and captures payment
	- On success, emits PAYMENT_COMPLETED event
 - Fulfillment & Order Processing (FedEx Integration)
  - Order Service sends fulfillment request to FedEx Order Processing API
	- FedEx processes order details for fulfillment tracking and downstream reconciliation
	- FedEx returns fulfillment acknowledgment and tracking reference
	- Order Service updates fulfillment status asynchronously
 - Customer Notification
  - Notification Service listens for GIFT_CARD_ISSUED and fulfillment events
	- Sends confirmation email and updates customer account with fulfillment status
 - Order Completion
  - Order Service transitions order to COMPLETED
	- System achieves eventual consistency across Order, Payment, Gift Card, and FedEx systems

---

## Challenges
- Coordinating multiple distributed services (order, payment, gift card, notification)
- Ensuring reliable order state transitions across asynchronous systems
- Handling payment failures, retries, and partial failures without impacting user experience
- Maintaining data consistency and traceability across services
- Delivering near real-time fulfillment for digital gift cards

---

## Key Responsibilities

- Led cross-functional teams responsible for Order Service, Payment Integration, Gift Card Service, and Notification Service.
- Did API development from scratch.
- Facilitated Agile ceremonies and coordinated cross-team dependencies to support continuous delivery.
- Defined end-to-end order lifecycle and state transitions (CREATED → PAID → ISSUED → COMPLETED) to ensure system clarity and observability.
- Collaborated with architects and engineers to design an event-driven workflow enabling loose coupling and scalability.
- Oversaw integration with third-party payment systems, ensuring secure and reliable transaction processing.
- Ensured idempotency, retry mechanisms, and failure handling for payment and notification flows.
- Partnered with Product Owners and UX teams to ensure timely customer notifications and visibility of gift cards in user accounts.
- Supported release planning, production readiness, and post-release monitoring.

---

## Metrics & Outcomes
- Enabled near-instant digital gift card delivery upon successful payment
- Reduced order fulfillment failures through clear state management and retries
- Improved customer experience with real-time email notifications and account visibility
- Delivered a scalable platform capable of handling peak promotional traffic
- Increased operational transparency through well-defined order and event tracking 

---

## Tool & Tech Stack
Java, Python, Spring Boot, Microservices, SQL, Docker, Jenkins, AWS,Postgres, Oracle,
Jira, Confluence, Agile/Scrum 

---

## Real Delivery Scenario

- Handling Payment Failures & Asynchronous Fulfillment
- Designed clear retry and compensation flows for payment and gift card issuance failures
- Ensured users received timely notifications without exposing internal system errors
- Maintained order consistency and prevented duplicate gift card issuance through idempotent processing 
