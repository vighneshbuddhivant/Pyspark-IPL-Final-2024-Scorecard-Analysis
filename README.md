# IPL Final 2024 Scorecard Analysis using PySpark

## Project Overview
In this project, I analyzed the **IPL Final 2024** between **Sunrisers Hyderabad (SRH)** and **Kolkata Knight Riders (KKR)** using **PySpark** on **Databricks**. The primary goal was to transform raw IPL data and build a comprehensive scorecard for the **first innings** of the final match, showcasing both **batting** and **bowling** performances.

This project demonstrates how to perform data analysis on complex sports datasets using PySpark, highlighting key data transformation techniques, aggregation, and handling schema-related issues.

## Key Highlights:
- Introduction to the IPL Final 2024 dataset
- Step-by-step guide to data transformation using PySpark
- Comprehensive **first innings batting** and **bowling scorecard** generation
- Handling missing values, calculating runs, wickets, strike rates, and bowling economy
- Challenges in working with large datasets and how they were overcome

## Technologies Used:
- **PySpark**
- **Databricks**
- **Apache Spark SQL**
- **Python**

## Dataset:
The dataset used for this project includes match deliveries for IPL matches. Key columns:
- `match_id`, `inning`, `batting_team`, `bowling_team`, `over`, `ball`, `batter`, `bowler`, `batsman_runs`, `extra_runs`, `total_runs`, `is_wicket`, etc.

The IPL final match is identified by `match_id = 1426312`.

## Project Structure:
1. **Schema Definition**: Defining the appropriate schema for the dataset and handling datatype issues.
2. **Filtering for IPL Final 2024**: Extracting data specific to the IPL Final match by filtering the correct match_id.
3. **First Inning Batting Scorecard**: 
   - Calculating runs, balls faced, boundaries (4s, 6s), and strike rate for each batter.
   - Sorting the scorecard based on batting order.
4. **First Inning Bowling Scorecard**:
   - Calculating overs bowled, runs conceded, wickets, economy rate, and maiden overs for each bowler.

## Results:
- Generated a **batting scorecard** for the first innings, including runs, balls faced, strike rate, and boundaries for each batter.
- Created a **bowling scorecard** with overs bowled, runs conceded, wickets, economy, and maiden overs for each bowler.
- Sorted the batting scorecard according to the actual batting order.

## Challenges:
- **Data Type Mismatch**: The `match_id` and other columns were initially read as strings. This caused incorrect filtering and sorting. We fixed this by explicitly defining the schema using `StructType`.
- **Handling Missing Values**: Some deliveries had missing data for extras or wickets, which required special handling in aggregations.

## Conclusion:
This project showcases how to build a detailed IPL scorecard using **PySpark** on **Databricks**, applying various data transformation techniques. It demonstrates the potential of PySpark in handling large datasets, like IPL match data, efficiently.
