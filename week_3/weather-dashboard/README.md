# Station — Glassmorphic Neon Weather Dashboard

An immersive, premium client-side weather station dashboard that fetches and visualizes real-time weather readings using the keyless Open-Meteo Geocoding & Forecast APIs.

---

## 🎨 Theme & Visual Design

The application features a modern **Glassmorphic Neon Dark Mode**:
* **Background:** Deep space-black (`#0B0F19`) overlaid with dual ambient backing glows: radial lavender/violet (`#8B5CF6` at `10% 20%`) and radial cyan (`#06B6D4` at `90% 80%`).
* **Panels:** Frosted, semi-transparent slate cards (`rgba(30, 41, 59, 0.45)`) utilizing CSS `backdrop-filter: blur(12px)` and delicate borders.
* **Accents:** Electric neon cyan (`#22D3EE`) for secondary widgets and metric controls; electric violet (`#A78BFA`) for highlight details.
* **Weather Icons:** Custom SVG symbols that glow with modern, high-contrast neon highlights matching the current condition.
* **Typography:**
  * **Headings:** [Space Grotesk](https://fonts.google.com/specimen/Space+Grotesk) (futuristic, geometric, crisp).
  * **Body Copy:** [Inter](https://fonts.google.com/specimen/Inter) (readable, standard).
  * **Telemetry/Data:** [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) (technical console look).

---

## ✨ Features

1. **Keyless API Fetching:** Fully integrates with the Open-Meteo free geocoding and forecast API endpoints without requiring API tokens.
2. **One-Click Local Telemetry:** Connects to the browser Geolocation API to instantly request current coordinates and report local weather.
3. **Recent Search Memory:** Retains an active in-memory collection of the last 5 searched cities as quick-click navigation chips.
4. **Dynamic Unit Converter:** Allows seamless switching between Celsius (°C) and Fahrenheit (°F) with immediate recalculation and reloading of active reports.
5. **Detailed Weather Breakdown:** Reports feels-like temperature, humidity levels, wind speed, and accurate sunrise/sunset times.
6. **3-Day Visual Forecast:** Visualizes weather progressions for today and the subsequent two days with custom weather conditions and temperature ranges.

---

## 🛠️ Technical Details

### File Structure
* [weather-dashboard.html](file:///d:/neurofive/neurofivesolutions-tasks/week_3/weather-dashboard/weather-dashboard.html): Main file containing layouts, style sheets, and async Javascript routines.

### APIs Integrated
* **Geocoding:** `https://geocoding-api.open-meteo.com/v1/search`
* **Forecast:** `https://api.open-meteo.com/v1/forecast`

### Core Technologies
* **Structure:** HTML5.
* **Styles:** CSS Custom Properties, backdrop filters, responsive grid styling, custom spin animations.
* **Routines:** Async/Await Fetch API, Geolocation API, browser local clock ticker.

---

## 🚀 Running Locally

No installation or configuration needed:
1. Open [weather-dashboard.html](file:///d:/neurofive/neurofivesolutions-tasks/week_3/weather-dashboard/weather-dashboard.html) in any modern browser.
2. Ensure you have an active internet connection to enable Open-Meteo fetching.
3. Search for any global city or click the location icon to fetch local data.
