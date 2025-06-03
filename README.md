# sqlalchemy-challenge
Module 10 Hoemwork

## Project Overview

This project involves analyzing climate data for Honolulu, Hawaii, using Python, SQLAlchemy, Pandas, and Matplotlib. The goal is to extract and explore climate trends, then build a Flask API to serve climate-related data from SQLite databases.

## Dependencies

* Python
* Jupyter Notebook
* SQLAlchemy
* Flask
* Pandas
* Matplotlib

## Part 1: Climate Analysis

This section focusues on analyxing and exploring climate data using SQLAlchemy and Pandas.

### Steps
 1. Connect to the Database
  * Use create_engine() to establish a connection to hawaii.sqlite.
  * Reflect database tables using automap_base().
  * Create references to station and maeasurement tables.
  * Create a session to interact with the database.
 2. Percipitation Analysis
  * Retrieve the most recent date in the dataset.
  * Query the last 12 months of precepitation data (date and prcp).
  * convert results into a Pandas DataFrame, sort by date, and plot the precipitation data.
  * Generate summary statistics for percipitation values.
3. Station Analysis
  * Query the total number of stations.
  * Identify the most-active stations by counting measurement entries.
  * Query temperature observations for the most-active station over the last 12 months.
  * Plot the temperature observations as a histogram.
4. Close the Session
  * Always close the session at the end of the notebook.

## Part 2: Flask Climate API

After analyzing the data, a Flask API is developed to serve climate data dynamically.

### API Endpoints:

  * /
    * Lists all available API routes.
  * /api/v1.0/precipitation
    * Returns JSON of precipitation data for the last 12 months.
  * /api/v1.0/stations
    * Returns JSON list of all stations in the dataset.
  * /api/v1.0/tobs
    * Returns JSON list of temperature observations for the most-active station in the last 12 months.
  * /api/v1.0/<start>
    * Returns JSON of minimum, average, and maximum temperature from the start date onwards.
  * /api/v1.0/<start>/<end>
    * Returns JSON of minimum, average, and maximum temperature for the date range.

## Run the Flask

1. Navigate to the project directory.
2. Run python app.py.
3. Access the API via http://127.0.0.1:5000/.

## Conclusion

This project showcases climate data exploration using SQLAlchemy ORM and visualization tools, followed by a dynamic Flask API for data retrieval. By completing this challenge, you gain hands-on experience in data engineering and web service development.



