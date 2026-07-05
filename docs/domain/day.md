# Day Model

Status: Draft  
Version: 0.1  
Last updated: 2026-07-05  

---

## Concept

A Day is a complete snapshot of everything relevant for a specific date.

It is not a calendar.  
It is not a schedule.  
It is a structured understanding of the day.

---

## Day Structure

A Day consists of the following components:

```text
Day
├── date
├── agenda[]
├── weather
├── meals[]
├── reminders[]
├── departureInfo
```

---

## Properties

### date

The date this Day represents.

- Type: ISO Date string (YYYY-MM-DD)

---

### agenda

A list of time-based events.

**AgendaItem**
- id
- title
- startTime
- endTime
- location (optional)
- type (work | school | activity | other)

**Rules**
- Always sorted by startTime  
- Represents “fixed time commitments”

---

### weather

Weather snapshot for the day.

**Weather**
- temperature
- condition
- windSpeed
- summary

**Rules**
- Should be human readable, not raw API data

---

### meals

Meals relevant to the family (e.g. school lunch).

**Meal**
- title
- description
- time (optional)

**Rules**
- Can be empty
- Should come from external sources when possible

---

### reminders

Lightweight awareness items.

Not tasks. Not actionable systems. Just “don’t forget this”.

**Reminder**
- text
- priority (low | medium | high)

**Examples**
- Bring gym clothes  
- Library books due today  

---

### departureInfo

Information about when the family needs to leave.

**DepartureInfo**
- latestLeaveTime
- reason
- travelTimeMinutes
- targetEvent (optional reference to agenda item)

**Rules**
- Derived data (computed in backend)
- Optional (can be null)

---

## Key Design Principle

The Day model is:

> Backend-owned, deterministic, and read-only for the frontend.

Frontend must never:
- compute
- infer
- modify

Only render.

---

## What this is NOT

The Day model is NOT:

- a database schema  
- a UI model  
- a user preference model  
- a real-time event stream  

---

## Future Extensions (intentionally excluded)

- personal views per family member  
- AI suggestions  
- confidence scoring of data  
- predictive planning  
