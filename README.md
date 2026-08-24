# Lab 1 — Requirements Engineering & UML Use-Case Modelling

**Problem Statement #10 — Student Club Event Ticketing & Budget Portal**
**Student:** Syed Junaid Ahmed
**Course:** Software Engineering, PES University (EC Campus)

## Overview

Student clubs need a single workflow to submit event proposals, route budget
requests through an approval hierarchy (Faculty Coordinator → Finance Office →
Dean), and issue secure QR-code tickets to attendees. This repo contains the
Lab 1 deliverables: a requirements table, a UML use-case diagram, and a
use-case flow specification.

**Target stakeholders / actors:** Club Lead, Faculty Coordinator, Finance
Officer, Dean, Attendee, Campus Admin.

## Contents

| File | Description |
|---|---|
| `Requirements_Table.docx` | 5 Functional Requirements (FR-001–FR-005) and 2 Non-Functional Requirements (NFR-001–NFR-002), each with ID, Type, Description, Priority, Acceptance Criteria, and Rationale. |
| `usecase_diagram.pdf` | UML use-case diagram (hand-built SVG version) showing all actors, 9 use cases, one `«include»` and one `«extend»` relationship. |
| `usecase_diagram_plantuml.pdf` | Same diagram rendered from PlantUML source, exported to PDF. |
| `UseCase_Flow.docx` | One-page flow specification for UC-02 (Request Budget Approval): preconditions, postconditions, main success scenario, and one alternate flow. |

## Requirements Summary

- **FR-001** (given): Route budget proposals through Faculty Coordinator → Finance Office → Dean.
- **FR-002:** Club Lead submits an event proposal with an itemized budget.
- **FR-003:** System generates a unique, single-use QR-code ticket per registered attendee.
- **FR-004:** Campus Admin scans a ticket at check-in; system marks it used.
- **FR-005:** Club Lead is emailed whenever proposal status changes.
- **NFR-001** (given): QR-ticket scan validates in under 100 ms.
- **NFR-002:** Budget-approval workflow is role-restricted (RBAC) with a 15-minute idle session timeout.

## Use-Case Diagram

Actors: Club Lead, Faculty Coordinator, Finance Officer, Dean, Attendee,
Campus Admin.

Relationships modelled:
- `Request Budget Approval` **«include»** `Route Approval Workflow`
- `Register for Event` **«include»** `Generate QR-Code Ticket`
- `Flag Duplicate/Invalid Entry` **«extend»** `Scan Ticket at Check-in`

## Use-Case Flow

Documented in detail for **UC-02 — Request Budget Approval**, including the
alternate flow triggered when any approver (Faculty Coordinator, Finance
Officer, or Dean) rejects the proposal.

## How the diagram was generated

1. `usecase_diagram.pdf` — hand-authored SVG (see `usecase_diagram.svg`),
   converted with `cairosvg`.
2. `usecase_diagram_plantuml.pdf` — equivalent diagram written in PlantUML
   (see `usecase_diagram.puml`), rendered via PlantText/PlantUML and exported
   to PDF.

## Peer Critique

_(Add notes here after the Lab 1 peer-review swap: clarity, testability, and
relevance feedback received on the requirements table, and revisions made in
response.)_
