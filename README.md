# Solar_panels_tracker

⸻

Solar Panel Tracking System

An intelligent AI-based system built using n8n that automatically adjusts solar panel angles according to real-time solar position and weather conditions, without requiring human control.

⸻

What is an AI Agent?

An AI Agent is a system designed to operate independently by performing three main tasks:

* Monitoring: Collects environmental data such as sunlight intensity and weather conditions
* Processing: Determines the most efficient angle for the solar panels
* Execution: Adjusts the panel position automatically based on the decision

In simple terms: it senses, decides, and acts.

⸻

Technologies Used

Tool	Role
n8n	Automates the workflow of the AI system
Open-Meteo API	Provides real-time weather and solar data
Node.js	Handles calculations and data processing

⸻

Project Location

Al Kharj, Saudi Arabia
Coordinates: (24.1556, 47.3346)

⸻

System Workflow

Weather API → n8n AI Agent → Decision Process → Panel Adjustment
       ↑                                         ↓
   Environmental Data        Optimal Angle or Stop (if wind is high)

Process Steps:

1. Data Collection
    The system retrieves solar radiation and wind speed data
2. Decision Making
    The agent calculates the optimal tilt angle for the panels
3. Action Execution
    The panels are adjusted, or movement is stopped if conditions are unsafe

⸻

Decision Logic

// Calculate panel angle
angle = radiation > 0 ? Math.min(90, radiation / 10) : 0;
// Safety condition
if (windSpeed > 50) {
  stopPanels = true;
}

⸻

Safety Feature

If wind speed exceeds 50 km/h, the system automatically stops panel movement to prevent potential damage.

⸻

Requirements

* n8n (self-hosted or cloud)
* Open-Meteo API (free, no API key required)
* Node.js

⸻
