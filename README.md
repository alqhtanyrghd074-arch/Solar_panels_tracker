# Solar_panels_tracker

# 🌞 Solar Panels Tracker | نظام تتبع الألواح الشمسية

An **AI Agent** built with **n8n** that autonomously controls solar panel angles based on real-time sun position and weather data — no human intervention needed.

وكيل ذكاء اصطناعي مبني على **n8n** يتحكم تلقائياً في زاوية الألواح الشمسية بناءً على موقع الشمس والطقس في الوقت الفعلي.

-----

## 🤖 What is an AI Agent? | ما هو الوكيل الذكي؟

An AI Agent is a system that:

- **Perceives** its environment (weather & solar data)
- **Decides** the best action (optimal panel angle)
- **Acts** autonomously (adjusts panels automatically)

الوكيل الذكي هو نظام يستشعر بيئته، يتخذ قرارات، ويتصرف تلقائياً.

-----

## 🔧 Built With | التقنيات المستخدمة

|Tool              |Purpose                       |
|------------------|------------------------------|
|**n8n**           |AI Agent workflow automation  |
|**Open-Meteo API**|Real-time weather & solar data|
|**Node.js**       |Data processing & calculations|

-----

## 📍 Location | الموقع

**Al Kharj, Saudi Arabia** (Lat: 24.1556, Lon: 47.3346)

-----

## ⚙️ How the Agent Works | كيف يعمل الوكيل

```
[Open-Meteo API] → [n8n Agent] → [Decision] → [Panel Adjustment]
      ↑                                              ↓
  Weather Data         Optimal Angle / Stop if Wind > 50 km/h
```

1. **Sense** — n8n fetches real-time solar radiation & wind speed
1. **Think** — Agent calculates optimal panel elevation angle
1. **Act** — Adjusts panel angle or stops movement for safety

-----

## 🧮 Agent Decision Logic | منطق القرار

```javascript
// If radiation exists → calculate angle
elevation = radiation > 0 ? Math.min(90, radiation / 10) : 0

// Safety rule → stop if wind is too strong
if (windSpeed > 50) → stopPanels = true
```

-----

## 🛑 Safety Feature | ميزة الأمان

If wind speed > 50 km/h → Agent automatically stops panels to prevent damage.

-----

## 📦 Requirements | المتطلبات

- n8n (self-hosted or cloud)
- Open-Meteo API (free, no key required)
- Node.js
