# Use Cases and Scenarios

## 1. Document Information

| Item | Details |
|---|---|
| Project Name | Computer Repair Service Management System |
| Document Type | Use Cases and Scenarios |
| Project Category | Business Analyst Portfolio Case Study |
| Version | 1.0 |
| Status | In Progress |

## 2. Purpose

This document describes how users interact with the proposed Computer Repair Service Management System.

It identifies the system actors, defines the main use cases, and documents the normal and alternative flows of selected business processes.

The use cases are based on the supplied academic project scenario. They will support the development of the use case diagram, activity diagram, class diagram, communication diagram, and quotation state machine.

## 3. System Overview

The proposed system will support the company's computer repair process, from customer eligibility verification and quotation preparation through servicing, payment, repair status tracking, and component collection.

The system will also support user account administration.

## 4. System Actors

An actor is a person or external role that interacts with the system to achieve a goal.

| Actor | Description | Main Responsibilities |
|---|---|---|
| Customer | A person requesting computer component repair services. | Requests repairs, reviews quotations, accepts or rejects quotations, makes payments, checks repair status, and collects components. |
| Cashier | An employee who manages customer service transactions. | Verifies eligibility, captures customer and component information, prepares quotations and agreements, records payments, and issues receipts. |
| Technician | An employee responsible for servicing components. | Performs repair work and updates repair statuses. |
| System Administrator | A person responsible for managing system user accounts. | Adds and removes technician and other user accounts. |

**Business Management** is an important stakeholder but is not included as a direct system actor in this version because the supplied scenario does not specify a particular system interaction for this role.

## 5. Use Case List

| Use Case ID | Use Case Name | Primary Actor |
|---|---|---|
| UC-01 | Verify Customer Eligibility | Cashier |
| UC-02 | Register Customer Details | Cashier |
| UC-03 | Submit Repair Request | Customer |
| UC-04 | Record Component and Service Details | Cashier |
| UC-05 | Generate Quotation | Cashier |
| UC-06 | Accept or Reject Quotation | Customer |
| UC-07 | Prepare and Accept Service Agreement | Cashier / Customer |
| UC-08 | Record Deposit and Generate Receipt | Cashier |
| UC-09 | Update Repair Status | Technician |
| UC-10 | Log In and Check Repair Status | Customer |
| UC-11 | Process Final Payment and Generate Receipt | Cashier |
| UC-12 | Collect Repaired Components | Customer |
| UC-13 | Manage User Accounts | System Administrator |

## 6. Detailed Use Cases

### UC-01: Verify Customer Eligibility

**Primary actor:** Cashier

**Goal:** Determine whether a customer may proceed with a repair application.

**Preconditions:**
- The customer has approached the company to request a repair service.
- The cashier is ready to begin the application process.

**Main flow:**
1. The cashier requests the customer's identification document.
2. The cashier checks whether the identification is valid.
3. The cashier verifies the customer's age.
4. The cashier determines whether the customer meets the eligibility rules.
5. If the customer is eligible, the process continues to customer information capture.

**Alternative flows:**
- **A1 — Invalid identification:** The customer does not provide acceptable identification. The cashier cannot proceed until the identification requirement is resolved.
- **A2 — Customer is not over 18:** The customer does not meet the age requirement. The application process is cancelled.
- **A3 — Eligibility cannot be confirmed:** The cashier pauses the application until the issue is clarified or resolved.

**Postconditions:**
- An eligible customer may proceed to the next step.
- An ineligible application is cancelled.

### UC-02: Register Customer Details

**Primary actor:** Cashier

**Goal:** Capture the customer's details for the repair application.

**Preconditions:**
- The customer has passed the eligibility verification process.

**Main flow:**
1. The cashier enters the customer's identification number.
2. The cashier enters the customer's name.
3. The cashier enters the customer's contact number.
4. The cashier reviews the information for accuracy.
5. The customer information is recorded.

**Alternative flows:**
- **A1 — Missing information:** The cashier requests the missing details before continuing.
- **A2 — Incorrect information:** The cashier corrects the details before the application proceeds.

**Postconditions:**
- Customer information is available for the repair request and quotation process.

### UC-03: Submit Repair Request

**Primary actor:** Customer

**Goal:** Request repair services for one or more computer components.

**Preconditions:**
- The customer has approached the company for repair services.
- Eligibility requirements have been satisfied.

**Main flow:**
1. The customer explains which component or components require repair.
2. The cashier records the repair request.
3. The customer discusses the required servicing with the cashier.
4. The customer communicates the desired collection period.
5. The repair request proceeds to component and service detail capture.

**Alternative flows:**
- **A1 — Customer withdraws the request:** The process stops before a quotation is accepted.
- **A2 — Component information is incomplete:** The cashier requests clarification before preparing the quotation.

**Postconditions:**
- A repair request is recorded for further processing.

### UC-04: Record Component and Service Details

**Primary actor:** Cashier

**Goal:** Capture the information required to prepare an accurate quotation and service agreement.

**Preconditions:**
- Customer eligibility has been confirmed.
- Customer information has been recorded.
- A repair request has been submitted.

**Main flow:**
1. The cashier records the relevant component details.
2. The cashier records the required servicing.
3. The cashier records the selected service options.
4. The cashier records the desired collection period.
5. The cashier reviews the information.
6. The information is made available for quotation preparation.

**Alternative flows:**
- **A1 — Missing component details:** The cashier requests additional information.
- **A2 — Customer changes service requirements:** The cashier updates the details before generating the quotation.

**Postconditions:**
- Component and service details are available for quotation preparation.

### UC-05: Generate Quotation

**Primary actor:** Cashier

**Goal:** Produce a quotation showing the proposed repair services and associated costs.

**Preconditions:**
- Customer details are recorded.
- Component and service details are available.
- Applicable pricing information is available.

**Main flow:**
1. The cashier reviews the customer details.
2. The cashier reviews the component and service information.
3. The cashier enters or confirms the applicable costs.
4. The system prepares a quotation containing customer details, component information, selected services, and costs.
5. The cashier presents or prints the quotation for the customer.

**Alternative flows:**
- **A1 — Pricing information is unavailable:** The quotation is paused until the required pricing information is confirmed.
- **A2 — Incorrect quotation details:** The cashier corrects the information before presenting the quotation.
- **A3 — Customer requests clarification:** The cashier explains the quotation before the customer makes a decision.

**Postconditions:**
- A quotation is available for the customer's decision.

### UC-06: Accept or Reject Quotation

**Primary actor:** Customer

**Goal:** Decide whether to proceed with the proposed repair services.

**Preconditions:**
- A quotation has been prepared and presented to the customer.

**Main flow:**
1. The customer reviews the quotation.
2. The customer decides to accept it.
3. The process continues to service agreement preparation and acceptance.

**Alternative flows:**
- **A1 — Customer rejects the quotation:** The cashier cancels the process.
- **A2 — Customer needs more information:** The customer requests clarification before deciding.
- **A3 — Customer requests a change:** The cashier reviews the requested change and determines whether a revised quotation is required.

**Postconditions:**
- An accepted quotation proceeds to the agreement and deposit stages.
- A rejected quotation results in cancellation of the process.

### UC-07: Prepare and Accept Service Agreement

**Primary actors:** Cashier and Customer

**Goal:** Document the agreed repair services and applicable terms and conditions.

**Preconditions:**
- The customer has accepted the quotation.

**Main flow:**
1. The cashier prepares the service agreement.
2. The agreement includes applicable servicing details and terms and conditions.
3. The agreement records collection arrangements and applicable theft or damage insurance options.
4. The cashier presents the agreement to the customer.
5. The customer reviews the agreement.
6. The customer signs or otherwise provides the required documented acceptance.
7. The process continues to deposit processing.

**Alternative flows:**
- **A1 — Customer does not accept the agreement:** The process is paused and the matter is referred for clarification.
- **A2 — Customer requests a correction:** The cashier reviews and corrects the agreement before acceptance.
- **A3 — Customer withdraws:** The application is stopped, subject to the applicable cancellation procedure.

**Postconditions:**
- An accepted service agreement is recorded.
- The application can proceed to deposit processing.

### UC-08: Record Deposit and Generate Receipt

**Primary actor:** Cashier

**Goal:** Record the customer's deposit and provide evidence of payment.

**Preconditions:**
- The quotation has been accepted.
- The service agreement has been accepted.
- The applicable deposit amount has been established.

**Main flow:**
1. The cashier confirms the deposit amount.
2. The customer pays the deposit.
3. The cashier records the payment.
4. The system generates a deposit receipt.
5. The receipt is provided to the customer.
6. The repair request proceeds to servicing.

**Alternative flows:**
- **A1 — Payment is unsuccessful:** The deposit is not confirmed, and the repair process does not proceed on the assumption that payment was received.
- **A2 — Deposit amount is unclear:** The cashier confirms the amount before completing the transaction.

**Postconditions:**
- The deposit is recorded and a receipt is generated.
- The repair process may proceed once the required conditions have been satisfied.

### UC-09: Update Repair Status

**Primary actor:** Technician

**Goal:** Keep repair information up to date.

**Preconditions:**
- A repair request has been accepted for servicing.
- The technician has access to the relevant repair information.

**Main flow:**
1. The technician identifies the relevant repair request.
2. The technician performs or assesses the repair work.
3. The technician updates the component status.
4. The status is recorded.
5. The repair status remains available for authorised users to view.

**Alternative flows:**
- **A1 — Component cannot be repaired:** The technician records the appropriate status, such as Not Fixed.
- **A2 — More work is required:** The technician keeps the status as In Process or updates it to another agreed status.
- **A3 — Incorrect status recorded:** The technician corrects the status, subject to applicable access controls.

**Postconditions:**
- The component's repair status reflects the latest recorded information.

### UC-10: Log In and Check Repair Status

**Primary actor:** Customer

**Goal:** View the status of a repair request.

**Preconditions:**
- The customer has an account or authorised login credentials.
- Relevant repair information has been recorded.

**Main flow:**
1. The customer opens the login facility.
2. The customer enters the required credentials.
3. The system verifies the login information.
4. The customer accesses the relevant repair information.
5. The customer views the recorded repair status.

**Alternative flows:**
- **A1 — Incorrect login details:** Access is denied, and the customer may try again.
- **A2 — Repair request cannot be found:** The customer is advised to contact the company for assistance.
- **A3 — Repair status has not been updated:** The system displays the available status information without implying that work has been completed.

**Postconditions:**
- The customer can view the available status information after successful authentication.

### UC-11: Process Final Payment and Generate Receipt

**Primary actor:** Cashier

**Goal:** Record the final payment after servicing is complete and the customer is satisfied.

**Preconditions:**
- Servicing has been completed.
- The customer has examined the components and confirmed satisfaction.
- The outstanding amount has been established.

**Main flow:**
1. The customer visits the company office.
2. The customer examines the serviced components.
3. The customer confirms satisfaction.
4. The cashier confirms the outstanding amount.
5. The customer pays by cash or credit card.
6. The cashier records the payment.
7. The system generates a final payment receipt.
8. The receipt is provided to the customer.

**Alternative flows:**
- **A1 — Customer is dissatisfied:** The payment process is paused while the issue is referred for resolution.
- **A2 — Payment is unsuccessful:** The payment remains outstanding until the transaction is successfully completed.
- **A3 — Outstanding amount is disputed:** The cashier checks the quotation, agreement, and payment records before proceeding.

**Postconditions:**
- The final payment is recorded and a receipt is issued when payment succeeds.

### UC-12: Collect Repaired Components

**Primary actor:** Customer

**Goal:** Collect the components from the company's designated office.

**Preconditions:**
- The components are available for collection.
- Applicable payment and collection requirements have been satisfied.

**Main flow:**
1. The customer visits the designated office.
2. The customer identifies the relevant repair request.
3. The cashier or authorised employee verifies the collection details.
4. The components are handed over to the customer.
5. The collection is recorded where the process supports collection tracking.

**Alternative flows:**
- **A1 — Components are not ready:** The customer is informed that collection cannot yet be completed.
- **A2 — Payment is outstanding:** Collection is handled according to the company's agreed payment policy.
- **A3 — Customer disputes the repair outcome:** Collection is paused while the concern is addressed.

**Postconditions:**
- The components are handed over and the collection is recorded where supported.

### UC-13: Manage User Accounts

**Primary actor:** System Administrator

**Goal:** Maintain the system's user accounts.

**Preconditions:**
- The administrator is authorised to manage user accounts.
- The system is accessible.

**Main flow:**
1. The administrator accesses user account management.
2. The administrator selects the required account action.
3. The administrator adds a new account or removes an existing account.
4. The system records the change.
5. The administrator confirms that the action was completed.

**Alternative flows:**
- **A1 — Unauthorised access:** The system denies access to account management.
- **A2 — Required account information is missing:** The system requests the missing information before an account can be created.
- **A3 — Account does not exist:** The system informs the administrator that the requested account cannot be found.

**Postconditions:**
- The account change is completed when the request is valid and authorised.

## 7. End-to-End Business Process

The main repair service process can be summarised as follows:

1. Customer approaches the company and requests repair services.
2. Cashier verifies identification and age eligibility.
3. If the customer is ineligible, the application is cancelled.
4. Cashier records customer details.
5. Customer explains the repair requirements.
6. Cashier records component and service details.
7. Cashier generates and presents a quotation.
8. Customer decides whether to accept the quotation.
9. If the quotation is rejected, the process is cancelled.
10. If accepted, the cashier prepares the service agreement.
11. Customer accepts the agreement.
12. Customer pays the required deposit and receives a receipt.
13. Technician performs the repair work and updates component statuses.
14. Customer logs in to check the recorded repair status when needed.
15. Customer visits the office to examine the serviced components.
16. If satisfied, the customer pays the outstanding amount and receives a receipt.
17. Customer collects the components.

This sequence is a high-level interpretation of the supplied scenario. Detailed exception handling and collection rules require stakeholder validation.

## 8. Key Business Process Decisions

| Decision | Possible Outcomes | Result |
|---|---|---|
| Is the customer eligible? | Yes / No | Continue or cancel the application. |
| Does the customer accept the quotation? | Accept / Reject | Continue to agreement or cancel the process. |
| Does the customer accept the service agreement? | Accept / Not accept | Continue to deposit processing or pause for clarification. |
| Can the component be repaired? | Fixed / Not Fixed / In Process | Record the appropriate repair status. |
| Is the customer satisfied with the completed repair? | Yes / No | Continue to final payment or pause for resolution. |
| Is payment successful? | Successful / Unsuccessful | Record payment and issue receipt, or leave payment unresolved. |

## 9. Relationship to UML Diagrams

The following diagrams will be developed to communicate the system analysis visually.

| Diagram | Purpose |
|---|---|
| Use Case Diagram | Shows the actors and their interactions with the system. |
| Activity Diagram | Shows the sequence of activities, decisions, and responsibilities across Customer, Cashier, System, and Technician. |
| Class Diagram | Shows the main business entities and their relationships. |
| Communication Diagram | Shows the interactions involved in creating an invoice or payment document. |
| Quotation State Machine | Shows how a quotation moves through its lifecycle. |

## 10. Assumptions and Items Requiring Validation

The following points require further clarification before the use cases can be treated as final requirements:

- The exact identification documents accepted by the company.
- Whether the age requirement excludes customers who are exactly 18 years old.
- Whether customers must create accounts before submitting repair requests.
- The precise quotation approval and revision process.
- The deposit amount, refund rules, and cancellation policy.
- The handling of components that cannot be repaired.
- The conditions under which a customer may collect components before final payment.
- The process for resolving customer dissatisfaction.
- Whether customer notifications are required when repair statuses change.
- How signatures and payment evidence are stored.

Where the original scenario does not specify a rule, this document records a proposed process or an open question rather than treating an assumption as a confirmed business requirement.

## 11. Document Status

This document is part of a Business Analyst portfolio case study based on an academic scenario. It demonstrates structured requirements analysis and process documentation; it does not claim that the proposed system has been implemented or deployed.

The use cases will be refined as the UML diagrams and supporting analysis are developed.
