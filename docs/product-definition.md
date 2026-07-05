# Product Definition

Status: Draft  
Version: 0.1  
Last updated: 2026-07-05  

---

## Purpose

This document defines what DayFlow is in practical terms,
what the MVP includes, and what is intentionally excluded.

It translates vision and philosophy into a concrete product scope.

---

## Product Summary

DayFlow is a family day overview system.

It aggregates information from existing services and presents a single, shared view of the current day.

It is not a system for managing tasks or data.

It is a system for **understanding the day at a glance**.

---

## MVP Scope (Phase 1–2)

The initial version of DayFlow includes:

### 1. Daily overview

A single “Today” view containing:

- Agenda (calendar events)
- Weather summary
- Meals (e.g. school lunch)
- Reminders
- Departure/time-to-leave information (basic calculation)

---

### 2. Data sources (initial integrations)

- Google Calendar (agenda)
- SMHI (weather)
- School meal API (or static source initially)
- Simple internal reminders

---

### 3. Display model

A structured Day View Model:

- Backend aggregates all data
- Frontend only renders the model
- No business logic in UI

---

## Explicit Non-Goals (MVP)

The following are NOT part of MVP:

- Personalization per user
- AI-generated recommendations
- Chat interface
- News feeds
- Smart home control
- Task management system
- Editing or managing external calendars
- Notifications system (push, email, etc.)

---

## Future Scope (post-MVP)

These are intentionally postponed:

- Personal perspectives (per family member)
- Insight engine (proactive suggestions)
- Morning/evening modes
- Voice interface
- Home assistant integration
- Predictive planning (e.g. “you should leave earlier”)
- Context-aware UI adjustments

---

## Core Constraint

DayFlow MVP must remain:

> Read-only, calm, and predictable.

It should never require user input to be useful.

---

## Success Criteria (MVP)

The MVP is successful if:

- A family can open DayFlow and immediately understand:
  - what is happening today
  - when they need to leave
  - what they need to prepare
- No one needs to “configure” it daily
- It reduces morning uncertainty

---

## Product Principle Alignment

This document enforces:

- Calm over complexity
- Shared first
- Integrate, don't replace
- Information over administration