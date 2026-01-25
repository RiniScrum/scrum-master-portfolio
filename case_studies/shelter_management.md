# 📌 Shelter Management System – Mission-Driven Non-Profit Platform

## Case Study Title
**Scaling Agile Delivery for a Mission-Driven Platform**

---

## Context
- **Domain:** Retail E-commerce
- **Teams:** 1–2 small Scrum teams  
- **Stakeholders:** NGOs, volunteers, operations teams  

---

## Project Overview

Designed and delivered a Shelter Management System enabling animal rescue operations, volunteer coordination, and daily shelter workflows. 
Implemented backend services, data models, and APIs to handle case management, scheduling, and operational reporting, ensuring scalability, 
reliability, and maintainability while optimizing resource usage and system performance.

---

## Role

Technical Project Manager & Architect

---
## Key Workflow – Wishlist, Checkout & Shelter Donation (GraphQL + Wizmo)

- Wishlist Management
 - Authenticated customer browses products and adds items to Wishlist Service.
 - Wishlist Service persists items and metadata (product ID, quantity, shelter eligibility).
- Wishlist to Checkout Transition
 - Customer selects items from wishlist and moves them to checkout.
 - Checkout Service retrieves wishlist items.
 - Cart and pricing validations are applied before checkout initiation.
- Checkout & Order Processing
 - Checkout Service orchestrates:
 - Pricing and tax calculation
 - Inventory validation
 - Payment authorization
 - Successful payment triggers order creation and fulfillment workflow.
- Donation Selection (Shelter Support)
  - During checkout, customer selects an optional donation to a shelter.
	- Donation amount and shelter details are captured as part of checkout context.
	- Donation data is decoupled from core order flow to avoid checkout latency.
- Donation Processing via GraphQL & Wizmo
  - Donation Service invokes Wizmo integration using GraphQL queries.
	- Wizmo processes the donation and returns transaction confirmation.
	- Donation status is asynchronously updated to ensure checkout completion is not blocked.
- Post-Checkout Updates
  - Order Service completes order lifecycle.
	- Wishlist items are removed or marked as purchased.
	- Customer receives confirmation including:
	  - Order details
	  - Donation acknowledgment
	  - Shelter information
- Observability & Reliability
  - Donation and checkout events logged and monitored via centralized logging.
	- Retry and idempotency mechanisms ensure donation requests are not duplicated.
  - Failures in donation flow do not impact order completion.

## Key Responsibilities

- Developed backend services and APIs for a mission-critical NGO platform, focusing on reliability, scalability, and maintainability.
- Implemented core business logic, persistence layers, and service integrations.
- Diagnosed and resolved production issues, improving system robustness and user experience.
- Participated in release execution and post-deployment validation.

---

## Challenges
- Limited resources and constrained budgets  
- Frequently changing stakeholder priorities  
- Small team bandwidth with multiple responsibilities  

---

## Metrics & Outcomes
- Improved sprint goal success rate despite resource constraints
- Reduced cycle time through simplified workflows
- Delivered usable, high-impact features faster
- Maintained high team engagement and morale  

---
