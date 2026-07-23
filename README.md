# SentryCore

**An IoT-based predictive maintenance system for industrial equipment**

## Problem
Across industries — manufacturing, agriculture, logistics, small workshops — equipment failure is usually caught too late, after a breakdown has already happened. Most operations rely on manual checks or scheduled maintenance, missing early warning signs that develop gradually. This leads to unplanned downtime, costly emergency repairs, and avoidable equipment damage.

## Solution
SentryCore uses ESP32 microcontrollers to continuously stream sensor data from machines in the field. This feeds a **Machine Health Index (MHI)** — a real-time score reflecting equipment condition — and a **Maintenance Priority Score (MPS)** ranking which machines need attention first, both surfaced on a live dashboard with early alerts.

## How It Works
Sensors → ESP32 controller → MHI computation → Dashboard + Alerts → Prioritized maintenance recommendation

## Why It's General-Purpose
The sensor-to-score pipeline isn't tied to one machine type or industry — it plugs into any equipment generating measurable condition signals (vibration, temperature, load, etc.), whether that's factory machinery, generators, or farm equipment.

## Build Plan
1. Wire up an ESP32 with a vibration/temperature sensor and get live readings
2. Compute a basic MHI score from sensor thresholds
3. Push data to a live dashboard for real-time visualization
4. Trigger a basic alert when risk crosses a defined threshold

## About
Built by Omotade Hezekiah Adeniyi, Engineering student at Yaba College of Technology (Yabatech).
