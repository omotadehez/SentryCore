# SentryCore

**An AI-powered predictive maintenance platform for industrial equipment**

## Team: Quantum Pioneers
- Omotade Hezekiah Adeniyi (Team Lead)
- Dada Daniel
- Bolajoko Aliyat
- Anwakuwo Christopher Marvin

## Problem
Across industries — manufacturing, agriculture, logistics, small workshops — equipment failure is usually caught too late, after a breakdown has already happened. Most operations rely on manual checks or scheduled maintenance, missing early warning signs that develop gradually. This leads to unplanned downtime, costly emergency repairs, and avoidable equipment damage.

## Solution
SentryCore uses ESP32-based IoT sensors to continuously monitor machine health across **four signal types** — vibration, acoustic pattern, electrical current draw, and temperature — computing a real-time **Machine Health Index (MHI)** and **Maintenance Priority Score (MPS)**. An AI layer (Google Gemini) translates this data into plain-language diagnoses that identify the dominant contributing factor and recommend specific action — readable by any technician, not just engineers.

## How It Works
Sensors (vibration, acoustic, current, temperature) → ESP32 → weighted MHI/MPS scoring → AI diagnosis (Gemini) → Live dashboard with contributing-factor breakdown and alerts

### Signal weighting
- Vibration — 35% (primary early indicator of mechanical wear)
- Acoustic anomaly — 25% (bearing/gear faults often surface here first)
- Electrical current deviation — 25% (Motor Current Signature Analysis)
- Temperature — 15% (slower-moving, confirms other signals)

## Why It's General-Purpose
The sensor-to-score-to-diagnosis pipeline isn't tied to one machine type or industry — it plugs into any equipment generating measurable condition signals, whether that's factory machinery, generators, or farm equipment.

## Why Wema Bank Should Care
When Wema Bank finances equipment — a generator, a production line — that machine becomes the collateral. Today, the bank only finds out a machine has failed after it stops working, by which point the business has stalled and the collateral's value has already dropped.

**SentryCore turns that blind spot into live data — a credit score for machines.**

Every monitored machine gets a real-time Machine Health Index (MHI) from 0–100, just like a credit score:
- **90–100:** Healthy. Loan collateral is safe.
- **40–60:** Deteriorating. Possible failure within weeks.
- **Below 40:** Critical. Failure imminent.

**What this unlocks for Wema Bank:**
- **Risk reduction** — see equipment failure risk before a borrower defaults, not after
- **Dynamic lending** — offer better rates to SMEs with consistently high MHI scores, since their collateral risk is verifiably lower
- **Automated covenants** — if a financed machine's MHI drops below a set threshold, the loan officer is automatically flagged — no more surprise bad debt

**Built for ALAT.** SentryCore is designed API-first, so it isn't a separate portal — the goal is to plug directly into ALAT for Business, alongside Wema's existing embedded-finance approach (as seen in its recent Duplo integration). A manufacturer checking their ALAT balance could see their equipment's health score in the same view.

**The ask:** a pilot partnership with Wema Bank to monitor equipment across 10 manufacturing SMEs through the Hackaholics accelerator — making collateral visible, predictable, and smart.

## Roadmap
Phase 2 will explore fluid condition monitoring (oil/hydraulic fluid analysis) and performance-output tracking (speed, throughput, power efficiency) for deeper diagnostic coverage — these require more specialized sensors than the current ESP32-based prototype.

## Live Demo
🔗 [SentryCore Live Demo](https://omotadehez.github.io/SentryCore/SentryCore_Live_Demo.html)

## Tech Stack
- Frontend: HTML/CSS/JavaScript (client-side, no backend required for this prototype)
- AI: Google Gemini API for natural-language diagnosis generation
- Hardware concept: ESP32 microcontrollers with vibration, acoustic, current, and temperature sensors

## Demo Video
🔗 [Loom walkthrough](#) — *link to be added*

## Note on API Key
This prototype calls the Gemini API directly from the client for demo purposes. In production, this would be routed through a backend/serverless function to keep the API key secure.
