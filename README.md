# LLM Scheduling Assistant — LLM Orchestration Platform

This repository contains an AI-powered scheduling system that integrates a Spring Boot backend with an LLM-based agent, enabling users to create calendar events via natural language and synchronize them with external services such as Notion.

This project combines:

- **LLM orchestration** (FastAPI): translate user intent into schema-validated actions/payloads
- **Backend services** (Spring Boot): REST APIs + persistence + external sync (e.g., Notion)
- **Reliability mechanisms**: retries, error handling, and idempotent execution to prevent duplicate writes

## Features

- Natural language → **Schema-validated actions/payloads** (LLM orchestration)
- Tool routing runtime to **validate and dispatch** requests to backend REST APIs
- Spring Boot layered architecture (Controller / Service / Repository) with JPA
- MySQL persistence
- External service synchronization (Notion API)
- Retry & failure handling for async/unstable integrations
- **Idempotency-Key** support to prevent duplicate writes under retries/replays
- Production-style config via environment variables (no secrets in code)
- One-command local DB setup via Docker

## Tech Stack

- Orchestration: **Python, FastAPI, Pydantic**
- Backend: **Java 21, Spring Boot, Spring Data JPA**
- Database: **MySQL (Docker)**
- Integrations: **Notion API**
- DevOps: **Docker, Docker Compose**
- Config: **Environment Variables**
