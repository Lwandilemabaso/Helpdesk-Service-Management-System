
# Requirements Specification

## 1. Document Information

| Item | Details |
|---|---|
| Project Name | Computer Repair Service Management System |
| Document Type | Requirements Specification |
| Project Category | Business Analyst Portfolio Case Study |
| Status | In Progress |
| Version | 1.0 |

## 2. Purpose

The purpose of this document is to define the functional requirements, non-functional requirements, business rules, and outstanding questions for the proposed Computer Repair Service Management System.

This specification is based on the supplied academic project scenario. It translates the business needs described in that scenario into structured requirements that can guide system analysis, design, and future development.

## 3. Business Overview

The computer repair company services computer components and requires an improved system to manage customer information, repair requests, quotations, service agreements, payments, repair progress, and component collection.

The proposed system should support communication between customers, cashiers, technicians, and the system administrator while improving the management and tracking of repair services.

## 4. Scope of Requirements

The requirements cover the following business processes:

- Customer eligibility verification and registration.
- Repair request and component information capture.
- Service option selection and collection planning.
- Quotation preparation and customer decision-making.
- Service agreement acceptance and deposit processing.
- Repair status updates by technicians.
- Customer access to repair status.
- Final payment and receipt generation.
- Component collection at the company office.
- User account administration.

## 5. Stakeholders and Users

| Stakeholder | Responsibility |
|---|---|
| Customer | Requests repairs, reviews quotations, accepts or rejects quotations, makes payments, checks repair progress, and collects components. |
| Cashier | Verifies customer eligibility, captures customer and component details, prepares quotations and agreements, processes payments, and issues receipts. |
| Technician | Performs repair work and updates component repair statuses. |
| System Administrator | Manages system user accounts, including adding and removing technicians and other users. |
| Business Management | Oversees repair service operations and business performance. |

## 6. Functional Requirements

Functional requirements describe what the proposed system must do.

### FR-01: Customer Eligibility Verification

The system must support the verification of a customer's valid identification and age before faulty components are added to the service checklist.

### FR-02: Customer Information Capture

The system must allow the cashier to capture the eligible customer's identification number, name, and contact number.

### FR-03: Repair Request Capture

The system must allow a customer to request repairs for one or more computer components.

### FR-04: Component and Service Details

The system must allow the cashier to record component details, selected service options, and the customer's desired collection period.

### FR-05: Quotation Generation

The system must generate a quotation containing relevant customer details, component information, selected services, and associated costs.

### FR-06: Quotation Decision

The system must support the customer's decision to accept or reject a quotation. If the customer rejects it, the cashier must be able to cancel the process.

### FR-07: Service Agreement Preparation

The system must support the preparation of a service agreement containing applicable terms and conditions, servicing details, collection arrangements, and theft or damage insurance options.

### FR-08: Service Agreement Acceptance

The system must support recording the customer's acceptance of the service agreement, including the required signature or documented confirmation.

### FR-09: Deposit Processing

The system must support recording the required deposit after the customer accepts the quotation and service agreement. A deposit receipt must be generated.

### FR-10: Repair Status Updates

The system must allow technicians to update the status of components. Example statuses include In Process, Fixed, and Not Fixed.

### FR-11: Customer Repair Status Access

The system must allow customers to log in and check the status of their repair requests.

### FR-12: Final Payment Processing

The system must support final payment after servicing has been completed and the customer has examined the components and confirmed satisfaction. Supported payment methods in the scenario are cash and credit card.

### FR-13: Receipt Generation

The system must generate receipts for applicable deposit and final payment transactions.

### FR-14: Component Collection

The system must support the collection of serviced components at the company's designated office.

### FR-15: User Account Administration

The system administrator must be able to add and remove technician and other user accounts.

### FR-16: Customer Login

The system must allow registered customers to log in to access relevant repair information and service status.

## 7. Non-Functional Requirements

Non-functional requirements describe expected qualities and operational characteristics of the system.

The following requirements are proposed recommendations for further validation. They are not all explicitly stated in the original scenario.

### NFR-01: Security

The system should protect customer information, payment records, and repair information against unauthorised access.

### NFR-02: Access Control

The system should restrict functions according to user roles. For example, technicians should update repair statuses, while user account administration should be restricted to authorised administrators.

### NFR-03: Data Accuracy

The system should maintain accurate customer, component, quotation, agreement, and payment records.

### NFR-04: Usability

The system should provide clear and understandable screens so that customers and employees can complete their tasks efficiently.

### NFR-05: Performance

The system should respond within acceptable time limits when users access customer records, quotations, and repair statuses. Specific performance targets require agreement with stakeholders.

### NFR-06: Reliability

The system should preserve recorded information and handle errors in a controlled manner.

### NFR-07: Auditability

The system should support appropriate tracking of important changes to repair statuses, quotations, and payment records.

### NFR-08: Maintainability

The system should be structured so that authorised developers can maintain and update it as business requirements change.

## 8. Business Rules

Business rules define conditions that govern how the business process operates.

| Rule ID | Business Rule |
|---|---|
| BR-01 | A customer must be over 18 years old to proceed with the service application, according to the supplied scenario. |
| BR-02 | Valid identification must be checked before faulty components are added to the service checklist. |
| BR-03 | If the customer does not meet the eligibility requirements, the application process must be cancelled. |
| BR-04 | The customer's identification number, name, and contact number must be captured for an eligible application. |
| BR-05 | A quotation must be prepared before the customer decides whether to proceed. |
| BR-06 | If the customer rejects the quotation, the cashier cancels the process. |
| BR-07 | If the customer accepts the quotation, the service agreement must be accepted and the required deposit paid before repair work proceeds. |
| BR-08 | Technicians must update component repair statuses as work progresses. |
| BR-09 | Final payment takes place after servicing is complete and the customer is satisfied with the components. |
| BR-10 | Components are collected at the company's designated office. |
| BR-11 | The scenario specifies cash and credit card as payment methods. |

## 9. Assumptions and Constraints

### 9.1 Assumptions

- The company has an office where customers can submit and collect components.
- Cashiers are responsible for capturing customer and repair request information.
- Technicians are responsible for updating repair progress.
- The system administrator manages user accounts.
- Customers require access to relevant repair status information.
- The proposed system is a case study and has not been confirmed as an implemented production system.

### 9.2 Constraints

- The original scenario does not provide detailed technical architecture or infrastructure requirements.
- Exact pricing, deposit calculations, and insurance costs have not been specified.
- Detailed security, performance, and data retention standards require stakeholder agreement.
- The project scope and requirements may change as outstanding questions are resolved.

## 10. Outstanding Questions

These questions should be clarified with business stakeholders before the requirements are finalised.

| Question ID | Question | Reason for Clarification |
|---|---|---|
| OQ-01 | Which identification documents are accepted? | To define the eligibility verification process. |
| OQ-02 | Does "over 18" mean strictly older than 18, or may an 18-year-old apply? | To remove ambiguity in the age rule. |
| OQ-03 | What happens when a component cannot be repaired? | To define the outcome, customer communication, and possible charges. |
| OQ-04 | How are service prices and deposits calculated? | To establish consistent quotation and payment rules. |
| OQ-05 | Can a quotation be changed after it has been issued? | To define quotation revision and approval controls. |
| OQ-06 | What is the deposit refund policy when a customer cancels? | To clarify financial and cancellation procedures. |
| OQ-07 | Should customers receive notifications when repair statuses change? | To determine communication requirements. |
| OQ-08 | How should components that are not collected be handled? | To define uncollected property procedures. |
| OQ-09 | How are theft and damage insurance options priced and recorded? | To clarify agreement and insurance information. |
| OQ-10 | What login and password rules should apply? | To establish appropriate access and security requirements. |
| OQ-11 | What happens if a customer is dissatisfied with the completed repair? | To define dispute resolution, rework, and payment handling. |
| OQ-12 | What evidence must be retained for payments and signed agreements? | To define recordkeeping and audit requirements. |

## 11. Requirement Traceability

The requirements will be connected to analysis and modelling artefacts as the project progresses.

| Requirement Area | Planned Supporting Artefact |
|---|---|
| Customer eligibility and repair request | Use Cases and Scenarios |
| Quotation and service agreement | Use Case Diagram and Activity Diagram |
| Repair workflow and status changes | Activity Diagram and Quotation State Machine |
| Customer, component, quotation, and payment information | Class Diagram |
| Cashier interactions during invoice creation | Communication Diagram |
| Development approach | Methodology Evaluation |

## 12. Acceptance Considerations

The proposed system requirements should be reviewed with stakeholders to confirm that:

- All essential business processes are represented.
- Each functional requirement is understandable and testable.
- Business rules are consistent with the agreed business process.
- Non-functional requirements have measurable targets where appropriate.
- Outstanding questions are resolved or formally recorded for later decision.
- Requirements can be traced to relevant use cases, process diagrams, and test scenarios.

## 13. Document Status

This document is a working requirements specification for a Business Analyst portfolio case study. It is based on the supplied academic scenario and includes proposed non-functional requirements that require validation.

It does not represent verified requirements from a real client or a deployed production system.

The document will be updated as the business process, use cases, and UML diagrams are developed.
