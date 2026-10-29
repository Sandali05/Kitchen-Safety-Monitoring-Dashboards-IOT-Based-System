# Smart Kitchen Monitoring Dashboard

A React + Firebase web app for monitoring a smart kitchen with real-time sensor data, alerts, and visual analytics.

## Project Structure

- `gas-dashboard-project/` - main frontend app (Vite + React)
- `gas-dashboard-project/src/pages` - dashboard pages (Overview, Temperature & Humidity, Gas, Fridge, Fire)
- `gas-dashboard-project/src/components` - reusable UI blocks, charts, alerts, and chatbot
- `gas-dashboard-project/src/hooks` - Firebase data hooks for each sensor domain

## Features

- Real-time Firebase Realtime Database integration
- Multi-page dashboard for core kitchen safety and appliance monitoring
- Trend charts, timeline charts, forecasts, gauge cards, and correlation analysis
- Alerts and recommendations panels
- Built-in Analytics Copilot chatbot with optional OpenAI-compatible API support
- Local context-aware chatbot fallback when remote LLM config is missing

## Tech Stack

- React
- Vite
- Firebase Realtime Database
- Recharts

## Getting Started

### 1) Install dependencies

```bash
cd gas-dashboard-project
npm install
```

### 2) Start development server

```bash
npm run dev
```

### 3) Build for production

```bash
npm run build
```

If these values are missing or unavailable, the chatbot automatically falls back to local context-aware responses.

## Firebase Setup

Update Firebase config in:

- `gas-dashboard-project/src/config/firebase.js`

Expected nodes include:

- `TempnHumData/latest`, `TempnHumData/history`, `TempnHumData/analysis`
- `gassensorData/latest`, `gassensorData/history`, `gassensorData/analysis`
- `FridgeDoor/latest`, `FridgeDoor/history`, `FridgeDoor/analysis`
- `fire_monitoring/latest`, `fire_monitoring/history`, `fire_monitoring/analysis`

## License

Add your preferred license (for example, MIT) in a `LICENSE` file.
