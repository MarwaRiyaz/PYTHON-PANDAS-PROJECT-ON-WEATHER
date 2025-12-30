# PYTHON-PANDAS-PROJECT-ON-WEATHER
Analysis of real-world weather data using Python &amp; Pandas. Performed EDA to identify temperature trends, visibility, wind patterns, and weather conditions.
🌦 Weather Data Analysis using Pandas – Python Project
📌 Objective
To analyze the weather dataset using Python and Pandas, perform exploratory data analysis (EDA), and extract insights from real-world data.
Technologies Used
•	Python
•	Pandas
•	Jupyter Notebook
•	Matplotlib/Seaborn (optional for plots)
________________________________________
🔽 Step 1 – Load the Dataset
import pandas as pd
df = pd.read_csv("Weather_Dataset.csv")
df.head()
✔ Output Observed
Data contains columns like Date/Time, Temperature, Dew Point, Humidity, Wind Speed, Visibility, Pressure, Weather condition.
________________________________________
🔍 Step 2 – Basic Information About Data
df.info()
df.describe()
✔ Insights
•	Dataset has ~8784 rows and 8 columns
•	Includes numerical & categorical values
•	No missing values found (dataset is clean)
________________________________________
🔎 Step 3 – Exploring Data with Questions
1. What are the unique weather conditions?
df['Weather'].unique()
Answer: Fog, Snow, Rain, Clear, Cloudy, Freezing Drizzle, Thunderstorms, etc.
________________________________________
2. How many times was the weather exactly Clear?
df[df['Weather']=='Clear'].shape[0]
Answer: Appeared approx 1326 times
________________________________________
3. Find number of times Wind Speed was exactly 4 km/h.
df[df['Wind Speed_km/h']==4].shape[0]
Answer: 474 occurrences
________________________________________
4. What is the mean visibility?
df['Visibility_km'].mean()
Answer: Average visibility ≈ 27.66 km
________________________________________
5. Maximum & Minimum Temperature recorded
df['Temp_C'].max(), df['Temp_C'].min()
Answer:
•	Max temp = 33°C
•	Min temp = -23°C
________________________________________
6. Show all records where Weather contains "Snow"
df[df['Weather'].str.contains('Snow')]
Answer: Shows rows with Snowy & Snow-showers conditions
________________________________________
7. Relationship: Temperature vs Wind Speed (optional plot)
import matplotlib.pyplot as plt
plt.scatter(df['Temp_C'], df['Wind Speed_km/h'])
plt.xlabel("Temperature")
plt.ylabel("Wind Speed")
plt.title("Temperature vs Wind Speed")
plt.show()
________________________________________
📊 Key Insights from Data
Observation	Interpretation
Most frequent weather	Fog & Clear conditions
Coldest temperature	-23°C
Hottest temperature	33°C
Avg humidity	~ 70-80% across year
Visibility mostly high	Avg ~ 27km, low during fog
Wind mostly calm	Speed often between 4–9 km/h
________________________________________
🚀 Conclusion
This project demonstrates how Pandas can be used to explore weather data, extract patterns and generate insights. The dataset clearly shows temperature, humidity, visibility and weather variations throughout the year.
This project can be extended further by adding:
✔ Visualization graphs
✔ Time-series analysis
✔ Weather trend forecasting using ML

