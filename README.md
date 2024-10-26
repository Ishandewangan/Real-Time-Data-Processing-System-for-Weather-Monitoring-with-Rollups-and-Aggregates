# Real-Time-Data-Processing-System-for-Weather-Monitoring-with-Rollups-and-Aggregates

## Overview
This project is a weather monitoring and alert system that periodically fetches weather data from the OpenWeatherMap API, calculates daily weather summaries, and triggers alerts if certain conditions are met (e.g., temperature exceeds a threshold). The system stores weather data in a SQLite database and provides visualizations for daily summaries, historical trends, and triggered alerts.

## Features
- Fetches real-time weather data for multiple cities.
- Stores daily weather summaries (average, max, min temperature, humidity, wind speed, and dominant condition).
- Triggers alerts when the temperature exceeds a configurable threshold for a set number of consecutive readings.
- Sends email notifications for triggered alerts.
- Visualizes daily weather summaries and historical trends.
- SQLite database to store historical data.

## Design Choices
- **Data Fetching:** The weather data is fetched using the OpenWeatherMap API for selected cities.
- **Database:** SQLite is used to store the weather summaries and alert triggers. This choice is made for simplicity and local storage.
- **Visualization:** Matplotlib is used to plot the daily summaries and historical trends.
- **Alerts:** Email alerts are sent using Python's `smtplib` when a temperature exceeds the defined threshold.
- **Scheduling:** The weather data is fetched at regular intervals using the `schedule` library.

## Installation

### Dependencies
To set up the project, you'll need the following:

1. **Python** (Version 3.8+)
2. **pip** - Python's package installer.

You can install the required dependencies using the following command:

  ```bash
  pip install -r requirements.txt

## Running the Application
1. **Clone the repository**:
  ```bash
   git clone <your-repository-url>
   cd Real-Time-Data-Processing-System-for-Weather-Monitoring-with-Rollups-and-Aggregates



