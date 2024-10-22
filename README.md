### README.md

# Projects Overview

This repository contains two projects: a Rule Engine API and a Weather Monitoring Dashboard. 

## Project 1: Rule Engine API

This project implements a simple rule engine using Flask and SQLAlchemy. It allows users to create, store, and evaluate rules based on user-defined conditions using a web interface.

### Features

- Create rules with conditions using a simple syntax.
- Evaluate rules against user-provided data in JSON format.
- An intuitive web interface to interact with the rule engine.

### Technologies Used

- Python
- Flask
- SQLAlchemy
- SQLite
- HTML/CSS/JavaScript

### Getting Started

#### Prerequisites

Make sure you have the following installed:

- Python 3.x
- pip (Python package installer)

#### Installation

1. **Clone the repository:**

   ```bash
   git clone 
   cd rule-engine-api
   ```

2. **Install the required packages:**

   ```bash
   pip install Flask SQLAlchemy
   ```

3. **Run the application:**

   ```bash
   python app.py
   ```

   The application will start on `http://127.0.0.1:5000`.

#### Directory Structure

```
/project-root
│
├── /static
│   ├── style.css
│   ├── script.js
│
├── /templates
│   └── index.html
│
└── app.py
```

### Usage

1. **Access the web interface:**

   Open your web browser and go to `http://127.0.0.1:5000`.

2. **Creating a Rule:**

   - Fill in the "Rule Name" and "Rule String" fields in the "Create Rule" section.
   - **Example:**
     - **Rule Name**: `age_rule`
     - **Rule String**: `(age > 30 AND department = 'Sales')`
   - Click the "Create Rule" button.

3. **Evaluating a Rule:**

   - Enter the "Rule Name" and user data in JSON format in the "Evaluate Rule" section.
   - **Example:**
     - **Rule Name**: `age_rule`
     - **User Data**:
       ```json
       {
         "age": 35,
         "department": "Sales"
       }
       ```
   - Click the "Evaluate Rule" button to see if the rule is satisfied.

### Examples

- **Create Rule Example:**
  - **Rule Name**: `salary_experience_rule`
  - **Rule String**: `((age > 30 AND department = 'Sales') OR (experience > 5 AND salary > 50000))`

- **Evaluate Rule Example:**
  - **User Data**:
    ```json
    {
      "age": 28,
      "department": "Marketing",
      "experience": 7,
      "salary": 60000
    }
    ```
  - This will return `True` as the second condition is satisfied.



## Project 2: Weather Monitoring Dashboard

This project implements a weather monitoring dashboard using Flask and OpenWeatherMap API. It allows users to view current weather conditions and daily summaries for multiple cities, providing real-time weather data visualization.

### Features

- Fetch and display current weather data for multiple cities.
- Store weather data in an SQLite database.
- Generate daily summaries with average, maximum, and minimum temperatures.
- Real-time updates with a user-friendly dashboard interface.

### Technologies Used

- Python
- Flask
- SQLite
- OpenWeatherMap API
- Chart.js (for data visualization)
- HTML/CSS/JavaScript

### Getting Started

#### Prerequisites

Make sure you have the following installed:

- Python 3.x
- pip (Python package installer)
- OpenWeatherMap API key (sign up for free at [OpenWeatherMap](https://openweathermap.org/api))

#### Installation

1. **Clone the repository:**

   ```bash
   git clone 
   cd weather-monitoring-dashboard
   ```

2. **Install the required packages:**

   ```bash
   pip install Flask requests matplotlib
   ```

3. **Set up your API key:**

   - Replace `YOUR_OPENWEATHERMAP_API_KEY` in `weather_monitoring.py` with your actual OpenWeatherMap API key.

4. **Run the application:**

   ```bash
   python weather_monitoring.py
   ```

   The application will start on `http://127.0.0.1:5000`.

### Directory Structure

```
/project-root
│
├── weather_monitoring.py
│
└── templates
    └── index.html
```

### Usage

1. **Access the web interface:**

   Open your web browser and go to "http://127.0.0.1:5000".

2. **Current Weather Display:**

   - The dashboard will automatically fetch and display the current weather for the defined cities every 5 minutes.

3. **Daily Summary:**

   - Daily summaries will show average, maximum, and minimum temperatures, along with the dominant weather condition.

### Examples

- **Daily Summary Example:**
  - The daily summary will show statistics like:
    ```
    Delhi: Avg 28.5°C, Max 35.0°C, Min 22.0°C, Dominant: Clear
    ```
