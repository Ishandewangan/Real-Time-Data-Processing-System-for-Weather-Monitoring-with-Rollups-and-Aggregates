# Real-Time-Data-Processing-System-for-Weather-Monitoring-with-Rollups-and-Aggregates

Overview
This project is designed to monitor real-time weather data from various cities, calculate daily summaries, send alerts for high temperatures, and display visual trends. The application fetches weather data using the OpenWeatherMap API and stores it in an SQLite database. Additionally, it sends email alerts when the temperature crosses a defined threshold.

Features
Real-time Weather Fetching: Collects weather data such as temperature, humidity, and wind speed for multiple cities.
Daily Summaries: Generates daily summaries with average, maximum, and minimum temperatures, humidity, and dominant weather conditions.
Temperature Alerts: Sends email alerts if the temperature exceeds a user-defined threshold for consecutive readings.
Data Visualization: Displays visual trends of weather data and triggered alerts using matplotlib.
Historical Trends: Stores and shows historical weather data from an SQLite database.
Design Choices
API Usage: The OpenWeatherMap API is used for fetching real-time weather data for various cities.
Database: SQLite is chosen for lightweight, local storage of weather data.
Alerts: Email alerts are sent using Gmail's SMTP server whenever the temperature exceeds a predefined threshold.
Scheduling: Python's schedule module is used to automate data fetching and report generation at regular intervals (e.g., every 5 minutes).
Visualization: Matplotlib is used to create visual representations of daily weather summaries and historical trends.
Error Handling: The program is designed to handle API request failures and database errors gracefully.
Dependencies
The following Python packages are required to run the application:

requests: To fetch weather data from the OpenWeatherMap API.
pandas: For data manipulation and aggregation.
matplotlib: For creating visual plots of weather data.
sqlite3: To store weather data in a local database.
smtplib: For sending email alerts via Gmail.
schedule: To schedule periodic data fetching.
logging: To log events and errors during execution.


To install these dependencies, run:

pip install -r requirements.txt

Application Workflow
Weather Data Fetching: At regular intervals, the application requests weather data for the specified cities from the OpenWeatherMap API.
Data Storage: The fetched data is stored in an SQLite database.
Daily Summaries: A daily weather report is generated at the end of each day, summarizing the average, max, and min temperatures, humidity, and wind speed.
Alerts: If the temperature exceeds a predefined threshold, an alert email is sent to the user.
Visualization: The system generates visual charts to display weather trends and temperature alerts.
