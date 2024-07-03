# Weather App

A simple weather app that allows users to search for weather data by city name.

## How it Works

The app uses two API calls to retrieve weather data:

- **Geocoding API**: The app uses the OpenWeatherMap Geocoding API to retrieve the latitude and longitude of the searched city.
- **Weather API**: The app uses the OpenWeatherMap Weather API to retrieve the current weather data for the searched city.

## Code Overview

The `fetchWeather()` function is the main entry point of the app. It:

1. Retrieves the search input value.
2. Displays an error message if the input is empty.
3. Calls the `getLonAndLat()` function to retrieve the latitude and longitude of the searched city.
4. Calls the `getWeatherData()` function to retrieve the current weather data for the searched city.

### The `getLonAndLat()` Function

- Constructs the Geocoding API URL with the search input value and API key.
- Makes a GET request to the API.
- Parses the response JSON data.
- Returns the latitude and longitude of the searched city.

### The `getWeatherData()` Function

- Constructs the Weather API URL with the latitude and longitude of the searched city and API key.
- Makes a GET request to the API.
- Parses the response JSON data.
- Displays the current weather data in the app.

The app also includes a clear button that allows users to clear the search input and reset the app.

## API Keys

You will need to obtain an API key from OpenWeatherMap to use this app. Replace the `apiKey` variable in the code with your own API key.

## Future Development

- Add error handling and display error messages to the user.
- Implement caching or storage to reduce the number of API requests.
- Add more features, such as displaying weather forecasts or allowing users to save favorite cities.
