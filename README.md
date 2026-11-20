# 🌤️ Weather API Project

A responsive web app that shows a **3-day weather forecast** for any city. It auto-detects the user's location on load, lets you search for a city, and offers live autocomplete suggestions. The background image changes dynamically based on the current weather condition.

## 🌐 Live Project

Check out the live version of the app here: **[Weather API — Live Demo](https://youssef-mostafa543.github.io/Weather-api/)**

## 🎬 Video Preview

[![Video Preview](https://img.shields.io/badge/▶%20Watch%20Demo-Google%20Drive-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1Mc9RFordztHfgipULExUrI-OcLrDFII6/view)

> Click the badge above to watch the full demo of the app in action.

## ✨ Features

- 🌍 **Auto-location detection** — detects your city via IP on page load.
- 🔍 **City search** — type any city and get the forecast instantly.
- 💡 **Autocomplete suggestions** — live suggestions powered by Geoapify.
- 📅 **3-day forecast** — today's detailed weather + 2 upcoming days.
- 🌦️ **Dynamic background** — background image switches between sunny / cloudy / rainy themes.
- 📱 **Responsive design** — works on desktop and mobile.
- 💨 **Wind info** — speed and direction displayed.

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Markup | HTML5 |
| Styling | Tailwind CSS v4 + custom CSS |
| Logic | Vanilla JavaScript (ES Modules) |
| Weather data | [WeatherAPI](https://www.weatherapi.com/) |
| Geolocation (IP) | [MapTiler](https://www.maptiler.com/) |
| Autocomplete | [Geoapify](https://www.geoapify.com/) |

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (for the Tailwind CLI)
- A modern browser

### Installation

```bash
# Clone the repository
git clone https://github.com/Youssef-Mostafa543/Weather-api.git
cd Weather-api

# Install dependencies
npm install
```

### Build the CSS

The project uses Tailwind CSS. Generate `src/output.css` with:

```bash
npx @tailwindcss/cli -i ./styles.css -o ./src/output.css --watch
```

### Run

Open `index.html` in your browser (or serve it with any static server):

```bash
npx serve .
```

## 📁 Project Structure

```
Weather-api/
├── index.html        # Main page
├── script.js         # App logic & API calls
├── styles.css        # Tailwind + custom styles
├── src/
│   └── output.css    # Generated Tailwind output
├── city.jpg          # Default background
├── cloud.jfif        # Cloudy background
├── rain.jfif         # Rainy background
├── sunny.jfif        # Sunny background
├── package.json
└── README.md
```

## 📚 What I Learned

Building this project helped me practice several core web-development concepts:

- **Async programming** — using `async`/`await` and `fetch` to call external APIs (WeatherAPI, MapTiler, Geoapify) and handle responses/errors gracefully.
- **Debouncing** — implementing a `debounce` function for the city search input to limit API calls while typing.
- **DOM manipulation** — dynamically updating the UI (forecast cards, icons, wind info, background image) based on fetched data.
- **Error handling** — checking `response.ok`, catching network errors, and showing fallback alerts to the user.
- **Responsive design** — using Tailwind CSS utilities + media queries to adapt the layout for mobile screens.
- **Separation of concerns** — keeping API logic, UI rendering, and event handling in distinct functions.
- **Working with third-party APIs** — reading documentation, constructing query URLs with keys/params, and parsing JSON responses.

## 📝 Notes

- Make sure `src/output.css` exists before opening `index.html`, otherwise styling will be missing.
- The autocomplete suggestions are limited to 5 results and are debounced by 400ms.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

Made with ❤️ by [Youssef-Mostafa543](https://github.com/Youssef-Mostafa543)