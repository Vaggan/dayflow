# Roadmap

Status: Draft  
Version: 0.1  
Last updated: 2026-07-05  

---

## Purpose

This roadmap defines the phased evolution of DayFlow.

It ensures we build in the correct order:
first clarity, then structure, then features.

Each phase must be stable before the next begins.

---

## Guiding Principle

> We do not move to the next phase until the current phase reduces real family uncertainty.

Not all features are equally important.

Only those that improve clarity of the day matter.

---

# Phase 1 — Product Definition (DONE)

Status: Completed in documentation phase

### Outcome

- Vision defined
- Philosophy defined
- Product scope defined
- Architecture defined

### Result

We now understand what we are building before writing code.

---

# Phase 2 — Core MVP (Build Foundation)

Status: Next

## Goal

Create a working system that can display a "Day View".

No polish. No personalization. No extras.

---

## Scope

### Backend

- Day Builder service
- Basic integrations:
  - Google Calendar (mock allowed initially)
  - Weather (SMHI or mock)
  - Static meal data
- API endpoint: `/day/today`

---

### Frontend

- Angular application
- Single "Today View"
- Render Day View Model
- Minimal UI logic

---

## Constraints

- No authentication (single household use)
- No personalization
- No notifications
- No editing capabilities
- No real-time updates

---

## Definition of Done

- A user can open the app
- They see a structured overview of the day
- Data is consistent and centralized

---

# Phase 3 — Data Reliability & Real Integrations

## Goal

Replace mocks with real integrations and improve data consistency.

---

## Scope

- Replace mock data with real APIs
- Improve integration robustness
- Introduce caching layer
- Add basic error handling per integration

---

## Outcome

DayFlow becomes reliable enough for daily family use.

---

# Phase 4 — Multi-Perspective Model

## Goal

Introduce the concept of “who is this for?”

---

## Scope

- Family member context (still simple)
- Shared vs personal view separation
- Filtered day view per user

---

## Outcome

Each person can see what matters specifically to them.

---

# Phase 5 — Intelligence Layer (Optional Future)

## Goal

Move from reactive to proactive system.

---

## Scope

- Suggestions (e.g. leave earlier warnings)
- Pattern recognition (routine detection)
- Context-aware highlights

---

## Important

This phase must NOT affect MVP complexity.

It is strictly future-oriented.

---

# Explicit Non-Roadmap Items (Rejected or Deferred)

The following are intentionally excluded:

- Chat interface
- Full task management system
- Social features
- Smart home control
- Notifications system (push/email)
- News or external content feeds
- AI assistant layer in MVP

---

# Success Philosophy

A phase is only complete if it:

> Reduces uncertainty for the family without adding complexity.

If it increases cognitive load, it is not done.

---

# Key Insight

DayFlow is not built by adding features.

It is built by removing uncertainty step by step.