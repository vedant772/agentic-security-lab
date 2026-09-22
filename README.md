# AI Agent Security Lab

> A lightweight security testing environment for identifying common security risks in AI agents and LLM-powered applications.

AI agents introduce security risks beyond traditional applications because they can interpret natural-language instructions, access external tools, retrieve data, maintain context, and potentially take actions on behalf of users.

This project is an experimental security engineering lab focused on detecting common attack patterns and producing structured security findings.

The current implementation uses a **rule-based security analysis engine** built with Python and FastAPI.

---

## ⚠️ Project Status

**Active Development**

### Currently Implemented

- Prompt injection detection
- Sensitive information / credential pattern detection
- Dangerous command detection
- Severity classification
- Evidence extraction
- Structured JSON security findings
- FastAPI REST API
- Interactive Swagger/OpenAPI interface

> **Important:** The current implementation detects suspicious input patterns. It does not execute detected commands or autonomously test external AI agents.

---

## Overview

The current system analyzes user input against multiple security detectors:

```text
User Input
     ↓
Security Agent
     ↓
┌───────────────┬──────────────────┬────────────────────┐
│               │                  │                    │
▼               ▼                  ▼                    │
Prompt       Sensitive         Dangerous               │
Injection    Information       Commands                │
Detection    Detection         Detection               │
│               │                  │                    │
└───────────────┴──────────────────┴────────────────────┘
                        ↓
                Structured Findings
                        ↓
                    JSON Output
