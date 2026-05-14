# Solar_panels_tracker

#  Solar Panels Tracker | نظام تتبع الألواح الشمسية

An **AI Agent** built with **n8n** that autonomously controls solar panel angles based on real-time sun position and weather data — no human intervention needed.



-----

## 🤖 What is an AI Agent? 
An AI Agent is a system that:

- **Perceives** its environment (weather & solar data)
- **Decides** the best action (optimal panel angle)
- **Acts** autonomously (adjusts panels automatically)



-----

## 🔧 Built With 

|Tool              |Purpose                       |
|------------------|------------------------------|
|**n8n**           |AI Agent workflow automation  |
|**Open-Meteo API**|Real-time weather & solar data|
|**Node.js**       |Data processing & calculations|

-----

## 📍 Location 

**Al Kharj, Saudi Arabia** (Lat: 24.1556, Lon: 47.3346)

-----

## ⚙️ How the Agent Works 

```
[Open-Meteo API] → [n8n Agent] → [Decision] → [Panel Adjustment]
      ↑                                              ↓
  Weather Data         Optimal Angle / Stop if Wind > 50 km/h
```

1. **Sense** — n8n fetches real-time solar radiation & wind speed
1. **Think** — Agent calculates optimal panel elevation angle
1. **Act** — Adjusts panel angle or stops movement for safety

-----

## 🧮 Agent Decision Logic 

```javascript
// If radiation exists → calculate angle
elevation = radiation > 0 ? Math.min(90, radiation / 10) : 0

// Safety rule → stop if wind is too strong
if (windSpeed > 50) → stopPanels = true
```

-----

## 🛑 Safety Feature 

If wind speed > 50 km/h → Agent automatically stops panels to prevent damage.

-----

## 📦 Requirements 

- n8n (self-hosted or cloud)
- Open-Meteo API (free, no key required)
- Node.js
