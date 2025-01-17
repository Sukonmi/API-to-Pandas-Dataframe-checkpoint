# NASA API Data Processing

# 🎯 What I am aiming for.
This project demonstrates how to consume NASA's public APIs to retrieve and process data.

# ➡️ [Dataset Link](https://api.nasa.gov/)

# ℹ️ Instructions.

1. **Generate Your API Key**: Go to the [NASA API Portal](https://api.nasa.gov/) and generate your API key.
2. **Setup Your Environment**: Install the required packages using:
    ```bash
    pip install requests pandas
    ```
3. **Store Your API Key**: Save your API key in a variable in your Python script.
4. **Request APOD Data**: Follow the documentation to get the Astronomy Picture of the Day (APOD) data and store it in a DataFrame.
5. **Preprocess Data**: Clean the data and prepare it for analysis.
6. **Export to CSV**: Save the cleaned DataFrame to a CSV file.

# Example Code

```python
import requests
import pandas as pd

api_key = 'YOUR_API_KEY'

# Request APOD data
apod_url = f'https://api.nasa.gov/planetary/apod?api_key={api_key}'
response = requests.get(apod_url)
data = response.json()
df = pd.DataFrame([data])
print(df)

# Preprocess asteroid data
asteroid_data = [...]  # Your asteroid data here
cleaned_data = [...]  # Clean the data
df_cleaned = pd.DataFrame(cleaned_data)
print(df_cleaned)

# Export to CSV
df_cleaned.to_csv('asteroids.csv', index=False)
print("DataFrame exported to 'asteroids.csv'")
```
