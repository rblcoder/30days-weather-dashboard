# 30 Days DevOps Challenge - Weather Dashboard

Day 1: Building a weather data collection system using AWS S3 and OpenWeather API

# My learnings

Converted the script into a rest API endpoint using FastAPI, which was able to get the weather data using OpenWeather API and store the same in S3

## Screenshot

S3 objects which contain the data from the weather API

![Alt S3 objects storing weather data](s3objects.png?raw=true "S3 objects storing weather data")

# Weather Data Collection System - DevOps Day 1 Challenge

## Project Overview
This project is a Weather Data Collection System that demonstrates core DevOps principles by combining:
- External API Integration (OpenWeather API)
- Cloud Storage (AWS S3)
- Infrastructure as Code
- Version Control (Git)
- Python Development
- Error Handling
- Environment Management

## Features
- Fetches real-time weather data for multiple cities
- Displays temperature (°F), humidity, and weather conditions
- Automatically stores weather data in AWS S3
- Supports multiple cities tracking
- Timestamps all data for historical tracking

## Technical Architecture
- **Language:** Python 3.x
- **Cloud Provider:** AWS (S3)
- **External API:** OpenWeather API
- **Dependencies:** 
  - boto3 (AWS SDK)
  - python-dotenv
  - requests

```markdown
## Project Structure
weather-dashboard/
  src/
    __init__.py
    weather_dashboard.py
  tests/
  data/
  .env
  .gitignore
  requirements.txt

## Setup Instructions
1. Clone the repository:
--bash
git clone https://github.com/ShaeInTheCloud/30days-weather-dashboard.git

3. Install dependencies:
bashCopypip install -r requirements.txt

4. Configure environment variables (.env):
CopyOPENWEATHER_API_KEY=your_api_key
AWS_BUCKET_NAME=your_bucket_name

4.Configure AWS credentials:
bashCopyaws configure

5. Run the application:
python src/weather_dashboard.py

What I Learned

AWS S3 bucket creation and management
Environment variable management for secure API keys
Python best practices for API integration
Git workflow for project development
Error handling in distributed systems
Cloud resource management
Made a rest API endpoint using fastAPI

## Run the app:

uvicorn src.main:app --reload

Access API using /docs

Endpoint:

POST /weather/{city}

Sample output:

{
  "city": "Bengaluru",
  "temp": 72.39,
  "feels_like": 72.19,
  "humidity": 61,
  "conditions": "few clouds"
}



