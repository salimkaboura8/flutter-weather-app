<div align="center">

# 🌦️ Flutter Weather App

**A multi-day weather forecast app for any city, powered by OpenWeatherMap**

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![OpenWeatherMap](https://img.shields.io/badge/OpenWeatherMap-EB6E4B?style=for-the-badge)

[📂 Source](lib) · [🧠 Cubit](lib/business_logic) · [🌐 Data](lib/data)

</div>

---

## 📖 Overview

A **Flutter** app that shows the weather forecast for any city. You type a city name, and the app fetches the forecast from the **OpenWeatherMap API** and displays it with weather icons and formatted dates. Loading, success and error states are handled by a **Cubit** (`flutter_bloc`).

## 🔄 How It Works

| Step | What happens |
|:---:|---|
| 1️⃣ | The user types a city name in the search field |
| 2️⃣ | `WeatherForecastCubit` emits a loading state and asks the repository for data |
| 3️⃣ | `WeatherForecastRepository` calls the OpenWeatherMap forecast endpoint over HTTP |
| 4️⃣ | The JSON is mapped to `WeatherForecastModel`, and the UI shows the forecast or an error |

## ✨ Highlights

| 🌐 Data | 🧠 State | 🎨 UI |
|---|---|---|
| OpenWeatherMap REST API<br>`http` package<br>Typed JSON models | Cubit with Loading / Loaded / Error states<br>Repository pattern | City search<br>Sun, cloud and rain icons<br>Dates formatted with `intl` |

## 🚀 Quick Start

```bash
git clone https://github.com/salimkaboura8/flutter-weather-app.git
cd flutter-weather-app

flutter pub get
flutter run
```

> 🔑 Put your own OpenWeatherMap API key in `lib/data/weather_forecast_data.dart`.

---

<div align="center">
Made with ❤️ by <a href="https://github.com/salimkaboura8">Salim Kaboura</a>
</div>
