# Domain Model

Status: Draft  
Version: 0.1  
Last updated: 2026-07-05  

---

## Purpose

This folder defines the core concepts of DayFlow.

It is the shared language between:
- backend (data construction)
- frontend (rendering)
- future systems (insights, personalization)

---

## Core Idea

DayFlow is built around one central concept:

> The Day

Everything in the system exists to describe or enrich a Day.

---

## Core Entities

- Day
- AgendaItem
- Weather
- Meal
- Reminder
- DepartureInfo

---

## Rules

- Domain models must be simple and stable
- They should not contain UI logic
- They should not depend on frameworks
- They should evolve slowly