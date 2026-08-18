# SentryCore

**An AI-powered predictive maintenance platform for industrial and business-critical equipment**

## Team: Quantum Pioneers
- Omotade Hezekiah Adeniyi (Team Lead)
- Dada Daniel
- Bolajoko Aliyat
- Anwakuwo Christopher Marvin

## Problem
Nigerian SMEs and businesses rely on machinery to operate, but banks like Wema have limited real-time visibility into the condition of equipment tied to asset-backed loans. Risk assessment today relies mostly on paperwork and periodic checks, not live data — meaning equipment failure, and the loan risk that comes with it, is often only discovered after the fact.

## Solution
SentryCore uses ESP32-based IoT sensors to continuously monitor equipment health, computing a real-time **Machine Health Index (MHI)** and **Maintenance Priority Score (MPS)**. An AI layer (Google Gemini) translates this data into plain-language diagnoses and recommended actions — readable by any technician, not just engineers.

## Pathway to Wema Bank's Ecosystem
SentryCore's live equipment health data can serve as a **real-time risk signal for asset-backed lending** — giving Wema Bank visibility into the condition of financed equipment, enabling better-informed loan terms and early risk detection for SME borrowers, rather than relying on static paperwork.

## How It Works
Sensors → ESP32 → MHI/MPS scoring → AI diagnosis (Gemini) → Live dashboard with alerts

## Live Demo
🔗 [SentryCore Live Demo](https://omotadehez.github.io/SentryCore/SentryCore_Live_Demo.html)

## Tech Stack
- Frontend: HTML/CSS/JavaScript (client-side, no backend required for this prototype)
- AI: Google Gemini API for natural-language diagnosis generation
- Hardware concept: ESP32 microcontrollers with vibration/temperature sensors

## Demo Video
🔗 [Loom walkthrough](#) — *link to be added*

## Note on API Key
This prototype calls the Gemini API directly from the client for demo purposes. In production, this would be routed through a backend/serverless function to keep the API key secure.
