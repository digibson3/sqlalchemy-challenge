SQLAlchemy Climate Analysis & Flask API
Overview
This project analyzes historical climate data for Honolulu, Hawaii using Python, SQLAlchemy, Pandas, and Matplotlib. The goal is twofold:

Perform data analysis and visualization on temperature and precipitation trends.

Develop a Flask API that serves climate data dynamically from a SQLite database.

Technologies Used
Python 3

Jupyter Notebook

Pandas

SQLAlchemy

Flask

Matplotlib

SQLite

Part 1: Climate Data Analysis
Using SQLAlchemy and Pandas, this section focuses on extracting insights from a historical climate dataset.

Steps:
Database Connection

Establish connection to hawaii.sqlite using SQLAlchemy’s create_engine.

Reflect tables using automap_base.

Map ORM classes to the Measurement and Station tables.

Create a session for database interaction.

Precipitation Analysis

Determine the latest date in the dataset.

Query precipitation data for the last 12 months.

Load results into a Pandas DataFrame.

Visualize precipitation over time and generate summary statistics.

Station Analysis

Count the total number of weather stations.

Identify the most active station (based on observation counts).

Query temperature observations for this station over the past year.

Visualize the temperature distribution using a histogram.

Session Management

Ensure the SQLAlchemy session is closed after database operations.

Part 2: Flask Climate API
This section builds a RESTful API using Flask to expose climate data endpoints.

Available API Routes:
/

Welcome message and list of available API routes.

/api/v1.0/precipitation

Returns a JSON dictionary of dates and precipitation values for the last 12 months.

/api/v1.0/stations

Returns a JSON list of all weather stations in the dataset.

/api/v1.0/tobs

Returns temperature observations for the most active station over the past year.

/api/v1.0/temp/<start>

Returns JSON with min, avg, and max temperature from the given start date to the end of the dataset.

/api/v1.0/temp/<start>/<end>

Returns JSON with min, avg, and max temperature for the specified date range.

Running the Flask App
Navigate to the project directory.

Activate your Python environment.

Run the Flask app:

bash
Copy
Edit
python app.py
Open a browser and visit:
http://127.0.0.1:5000/

Project Highlights
Applied SQLAlchemy ORM techniques to reflect and query a real-world dataset.

Performed climate trend analysis using Pandas and Matplotlib.

Developed a fully functional Flask API to serve climate data on demand.

Gained experience in full-stack data workflows: from raw data analysis to web-based delivery.
