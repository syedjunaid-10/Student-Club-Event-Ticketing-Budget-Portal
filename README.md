# Student Club Event Ticketing & Budget Portal

**Problem Statement #10 — Campus & Academic Operations**[cite: 19]  
**Student:** Syed Junaid Ahmed (`PES2UG24AM166`, Sec 5C)  
**Course:** Software Engineering, PES University (EC Campus)[cite: 22]

---

## Overview
Student clubs require an integrated workflow to submit event proposals, route budget allocations through an approval hierarchy (**Faculty Coordinator → Finance Office → Dean**), and issue cryptographically signed QR-code tickets to attendees[cite: 19, 22]. This repository houses the Software Engineering lab deliverables for this system[cite: 22].

**Target Stakeholders / Actors:** Club Lead, Faculty Coordinator, Finance Officer, Dean, Student Attendee, Campus Admin[cite: 22].

---

## Repository Contents

### Lab 1 — Requirements Engineering & UML Use-Case Modelling[cite: 13]
| File | Description |
| :--- | :--- |
| `Requirements_Table.pdf`[cite: 22] | 5 Functional Requirements (`FR-001`–`FR-005`) and 2 Non-Functional Requirements (`NFR-001`–`NFR-002`) with ID, Type, Description, Priority, Acceptance Criteria, and Rationale[cite: 19, 22]. |
| `usecase_diagram.pdf`[cite: 22] | UML use-case diagram modeling all actors, primary use cases, and `<<include>>` / `<<extend>>` relationships[cite: 19, 22]. |
| `UseCase_Flow.pdf`[cite: 22] | One-page use-case flow specification detailing preconditions, postconditions, main success scenario, and alternate flows[cite: 19, 22]. |

### Lab 3 — Component Modelling & Architectural Pattern Selection[cite: 6]
| File | Description |
| :--- | :--- |
| `Lab3/Component_Diagram.png` | UML 2.5 component diagram using a **Layered Architecture** (Presentation, Business, and Data layers) with 6 components, ball-and-socket interfaces, and `<<use>>` dependencies[cite: 7, 10, 21]. |
| `Lab3/Justification.pdf` | One-page architectural justification detailing Layered Architecture selection, sequential approval enforcement, RBAC/TLS security, and `< 100 ms` QR validation performance[cite: 10, 12, 19]. |
