# Architecture

Status: Draft  
Version: 0.1  
Last updated: 2026-07-05  

---

## Purpose

This document describes the high-level system architecture of DayFlow.

It defines how data flows through the system and where responsibility lives.

The goal is to ensure that:

- the frontend remains simple
- business logic is centralized
- integrations are isolated
- the system remains evolvable over time

---

## Core Architectural Principle

> The backend defines the day.  
> The frontend displays the day.

This separation is fundamental to DayFlow.

---

## System Overview

DayFlow is structured into four main layers:

### 1. Integrations Layer

Responsible for communicating with external systems.

Examples:
- Google Calendar
- SMHI weather service
- School meal data sources

Responsibilities:
- Fetch raw data
- Normalize external formats
- Avoid business logic

---

### 2. Day Builder (Core Logic)

This is the heart of DayFlow.

It:
- collects data from integrations
- transforms it into a unified model
- builds the "Day View Model"

Responsibilities:
- aggregation
- light computation (e.g. time-to-leave)
- structuring data for UI

It does NOT:
- personalize per user (MVP)
- make subjective recommendations (MVP)
- manage UI concerns

---

### 3. API Layer

Exposes the Day model to clients.

Responsibilities:
- serve `/day/today`
- handle authentication (future)
- version API responses
- remain thin (no business logic)

---

### 4. Frontend (Angular)

A pure rendering layer.

Responsibilities:
- display the Day View Model
- organize UI components
- handle layout and presentation

It does NOT:
- fetch external data directly
- calculate business logic
- interpret meaning of data

---

## Data Flow

```text id="flowarch1"
External APIs
    ↓
Integrations Layer
    ↓
Day Builder
    ↓
API Layer
    ↓
Frontend (Angular)
    ↓
User sees "Today"