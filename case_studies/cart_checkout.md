# 📌 Cart & Checkout - High-Traffic E-commerce Core System

## Case Study Title
**Improving Checkout Stability and Release Confidence**

---

## Context
- **Domain:** Retail E-Commerce  
- **Teams:** 2 Scrum teams  
- **Users:** High-traffic transactional flows  

---

## Project Overview

Led Agile delivery of a high-traffic Cart & Checkout platform supporting critical e-commerce transactional flows, with a strong focus on checkout 
stability, performance, and release confidence.

---

## Role

Technical Project Manager & Architect

---

## End to End Checkout Flow
End-to-End Checkout Flow

- Cart Management
 - Customer adds/updates items in cart
 - Cart Service calculates totals and validates pricing rules
- Checkout Initiation
 - Checkout Service validates cart, user, shipping, and payment details
 - Inventory Service reserves stock to prevent overselling
- Pricing & Promotions
 - Pricing Service applies discounts, promotions, taxes, and fees
 - Checkout Service validates final payable amount
- Payment Processing
 - Checkout Service invokes external Payment Gateway
 - Payment is authorized and captured
 - On success, transaction status is returned to Checkout Service
- Order Creation
 - Order Service creates order and persists transactional state
 - Cart is cleared post successful order creation
- Post-Checkout Monitoring
 - Checkout and order metrics published to monitoring tools
 - Alerts triggered for latency, error rates, or payment failures

## Key Responsibilities

- Led 2 cross-functional Scrum teams delivering performance-sensitive checkout workflows.
- Facilitated Scrum ceremonies, backlog refinement, sprint planning, and cross-team coordination.
- Introduced a backlog readiness checklist and improved story slicing around end-to-end user journeys to increase sprint predictability.
- Oversaw end-to-end technical delivery, including checkout APIs, database changes, CI/CD pipelines (Jenkins), deployment readiness, and release coordination.
- Monitored production stability and service health using Datadog, Dynatrace, and Splunk logs, enabling faster detection and resolution of checkout-related issues.
- Led incident response during in-sprint production issues, facilitating sprint re-planning while maintaining team morale and stakeholder trust.

___

## Challenges
- Performance-sensitive checkout workflows  
- Frequent production incidents impacting releases  
- Incomplete or poorly refined user stories entering sprint planning
- Balancing defect resolution with feature delivery

---

## Metrics & Outcomes
- Reduced checkout-related production defects by 35%
- Improved release confidence with fewer emergency hotfixes
- Achieved more stable and predictable sprint commitments
- Faster incident resolution through improved monitoring and transparency 

---
## Tools & Tech Stack

Java, Spring Boot, Microservices, SQL, Docker, Jenkins, AWS,
Datadog, Dynatrace, Splunk, Jira, Confluence, Agile/Scrum

---
