Explanation of Each of the Files
1. Plot.ipynb
  Objective: Visualizes R-squared values for each rack across different days for a specific sensor.

  Steps:
    Reads CSV files for each rack.
  
    Filters data based on a selected sensor.
  
    Stores R-squared values, then plots R-squared values across days for each rack using a distinct color.
    
    Customizes the plot with labels, a title, and a legend.

3. Min_Max.ipynb
  Objective: Calculates minimum and maximum R-squared values and the respective days for each sensor across racks.

  Steps:

    Iterates through 20 racks, each having multiple CSV files.
  
    Groups data by sensor and identifies the min and max R-squared values.
  
    Stores these values with the corresponding rack, sensor, and day information.
  
    Saves the results as a combined DataFrame.

4. Metric_Calculation_For_Each_Rack.ipynb
  Objective: Calculates error metrics (MAE, MSE, RMSE, R-squared) using Random Forest Regression for different intervals.

  Steps:
    Defines date intervals and loads CSV data for each interval.
  
    Processes each sensor, extracting date, time, and calculating total seconds since midnight and day of the year.
  
    Splits the data into training and testing sets.
  
    Trains a Random Forest model and calculates error metrics for each day.
  
    Aggregates and displays results for each interval.


Implementation Outline
1. Data Loading & Preprocessing:
   Load sensor data for each rack and interval from CSV files.
   
   Process date and time to compute total seconds and day of the year.
   
   Convert values to numeric, handling missing values.
   
3. Model Training & Metric Calculation:
   Implement Random Forest and AdaBoost regression models on the sensor data with an 80:20 train-test split.
   
   Compute metrics: Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Square Error (RMSE), and R-squared.
   
   Tabulate the results for each sensor.
