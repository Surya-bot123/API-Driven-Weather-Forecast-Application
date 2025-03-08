
# API-Driven Weather Forecast Application

This is a simple Weather Forecast application built using HTML, CSS, and JavaScript.  he app allows users to check the current weather conditions of a city. It fetches weather data from the
OpenWeatherMap API and presents it in a user-friendly interface.

## Features

- City search: Users can search for weather data by entering the   city name.
- Real-time weather: Displays the current weather data such as temperature, humidity, wind speed, and weather conditions.
- Dynamic weather icons: Displays different icons for weather conditions like clear skies, rain, clouds, etc.
- Error handling: Shows an error message when an invalid city name is entered.
- Responsive: Optimized for both desktop and mobile devices.



## Acknowledgements

 - OpenWeatherMap: The weather data is provided by OpenWeatherMap, a free service offering global weather data.
     Website: https://openweathermap.org  
     API Documentation:https://openweathermap.org/api
    
 - [Font Used](https://fonts.google.com/specimen/Poppins)
 - [Weather Icons:](https://www.iconfinder.com/)


## API Reference
The application uses the OpenWeatherMap API to retrieve the weather data. It is a popular service that provides real-time weather information for any location worldwide.
#### OpenWeatherMap API

* API Documentation: https://openweathermap.org/api
* API Key: To use the API, you need to generate an API key.
    * Visit https://openweathermap.org/OpenWeatherMap and create an account.
    * After signing up, generate a free API key.
    * Replace the placeholder ```bash YOUR_API_KEY ``` in the ``` bash script.js ``` file with the API key.
#### Sample API Request URL:
https://api.openweathermap.org/data/2.5/weather?units=metric&q={city_name}&appid={API_KEY}
This URL is used to fetch the weather details for a given city. The ````bash appid={API_KEY} ``` is the authentication token that connects the app with OpenWeatherMap’s services.

## Installation 
Follow these steps to run the Weather App on your computer:
### Requirements:
A web browser (like Chrome or Firefox).   
An API key from OpenWeatherMap 
#### Steps:
1. Clone the Repository: Open your terminal and run this command to download the project:
git clone ``` https://github.com/your-username/weather-app.git ``` 

2. Go to the Project Folder: Navigate to the project folder:
```bash
  cd weather-app
```

3. Get Your API Key:
    * Go to OpenWeatherMap
    * Sign up and get your free API key   

4. Add the API Key: Open the ``` sript.js ``` file and replace ``` YOUR_API_KEY ``` with the key you got from OpenWeatherMap: 
```bash const apikey = "YOUR_API_KEY";   // Replace with your API key ```

Open the ```index.html ``` File: Double-click the ```index.html ``` file to open it in your browser.
#### Test the App:
Type a city name in the search box and click "Search" to see the weather!


    
## Appendix
### Project Structure
Here is a breakdown of the files and folders in this project:
``` bash
/weather-app
│
├── index.html        # Main HTML file that contains the structure of the web page.
├── style.css         # CSS file that handles the visual appearance and layout of the app.
├── script.js         # JavaScript file that interacts with the OpenWeatherMap API and updates the weather details.
├── /images           # Folder containing images used for weather icons and other assets.
│   ├── rain.png      # Icon for rain weather.
│   ├── clear.png     # Icon for clear weather.
│   ├── clouds.png    # Icon for cloudy weather.
│   ├── drizzle.png   # Icon for drizzle weather.
│   ├── mist.png      # Icon for misty weather.
│   ├── humidity.png  # Icon representing humidity.
│   └── wind.png      # Icon representing wind speed.
└── README.md         # This file, providing documentation for the project.

```
#### How the App Works
1. User Inputs a City Name:
* The user types a city name into the search box and clicks the search button.
2. JavaScript Fetches Weather Data:
* The app uses JavaScript's ``` fetch()``` function to send a request to the OpenWeatherMap API, requesting weather information for the entered city.
* The request URL looks like this:
``` https://api.openweathermap.org/data/2.5/weather?units=metric&q={city_name}&appid={API_KEY} ```

3. API Response:
* The API returns weather data in JSON format, which contains details such as temperature, humidity, wind speed, and weather conditions (e.g., rain, clear skies, etc.).
4. Displaying the Data:
* The app updates the DOM (Document Object Model) with the fetched weather data. This includes the city name, temperature, humidity, wind speed, and a corresponding weather icon.
* For example, if the weather condition is "Rain", the app will display a rain icon.
5. Error Handling:
* If the city entered doesn't exist or is invalid, the app displays an error message: "Invalid city name".
### API Details
* The app uses the OpenWeatherMap API to get weather data.
* The API provides current weather data, including temperature, humidity, wind speed, weather conditions, etc.
* API Endpoint: The base URL for the API is:
``` https://api.openweathermap.org/data/2.5/weather?units=metric&q={city_name}&appid={API_KEY} ```
* Parameters:
    * ``` q={city_name} ```: The name of the city to get the weather data for.
    * ``` appid={API_KEY} ```: The API key used for authentication.
    * ``` units=metric ```: This specifies the temperature units (Celsius in this case)
##### API Response Example: The API will return data in the following format:
```
{
  "name": "London",
  "main": {
    "temp": 15.2,
    "humidity": 80
  },
  "wind": {
    "speed": 10.5
  },
  "weather": [
    {
      "main": "Clear",
      "description": "clear sky"
    }
  ]
}
```
The app uses this data to display:

    * Temperature: 15.2°C
    * Humidity: 80%
    * Wind Speed: 10.5 km/h
    * Weather Condition: Clear sky (this determines the weather icon to display).
### Icons and Images
The app uses different icons to represent various weather conditions. These icons are stored in the ``` images/ ``` folder:
* rain.png: Represents rainy weather.
* clear.png: Represents clear or sunny weather.
* clouds.png: Represents cloudy weather.
* drizzle.png: Represents light rain or drizzle.
* mist.png: Represents misty or foggy weather.
* humidity.png: Represents humidity.
* wind.png: Represents wind speed.
#### Error Handling
The app shows an error message if the city name entered is invalid or does not exist in the OpenWeatherMap database. If an invalid city is entered:
* The app hides the weather display and shows the error message: "Invalid city name".
#### Customizing the App
1. Changing the Weather Icons:
You can replace the weather icons (stored in the ``` images/ ``` folder) with your own icons or use a different set of weather icons.
2. Changing the API Key:
* To use your own OpenWeatherMap API key, sign up on their website, generate a key, and replace ``` YOUR_API_KEY ``` in the ``` script.js ``` file with your own API key.
3. Styling the App:

* You can modify the ``` style.css ``` file to change the design of the app. For example, you can adjust the colors, fonts, and layout.
4. Adding Features:
* You could add a 7-day forecast or allow users to get the weather based on their location using the browser's geolocation API.



## API Reference
The application uses the OpenWeatherMap API to retrieve the weather data. It is a popular service that provides real-time weather information for any location worldwide.
#### OpenWeatherMap API

* API Documentation: https://openweathermap.org/api
* API Key: To use the API, you need to generate an API key.
    * Visit https://openweathermap.org/OpenWeatherMap and create an account.
    * After signing up, generate a free API key.
    * Replace the placeholder ```bash YOUR_API_KEY ``` in the ``` bash script.js ``` file with the API key.
#### Sample API Request URL:
https://api.openweathermap.org/data/2.5/weather?units=metric&q={city_name}&appid={API_KEY}
This URL is used to fetch the weather details for a given city. The ``` bash appid={API_KEY} ``` is the authentication token that connects the app with OpenWeatherMap’s services.
## Tech Stack
### Frontend
* HTML: Used to structure the content of the app, including input fields, buttons, and displaying weather information.
* CSS: Used for styling the app with a clean, modern look, and responsive design to make the app work well on both mobile and desktop devices.
* JavaScript: Utilized for dynamic content rendering, such as fetching weather data from the API, handling user input, and updating the DOM.
### APIs
* OpenWeatherMap API: Used to retrieve weather data (temperature, humidity, wind speed, etc.) for a specified city. The API allows us to access real-time weather information in a simple JSON format.
### Tools & Libraries
* Git: Used for version control and keeping track of the codebase throughout the development process.
* GitHub: Used to store the project code and collaborate on version control. GitHub Pages for deployment.
* Visual Studio Code: The text editor used for coding, with support for JavaScript, HTML, and CSS development.
## Lessons learned


Building the Weather Forecast Application taught me valuable lessons in web development. I learned how to integrate an external API, OpenWeatherMap, using JavaScript’s `fetch()` function to retrieve real-time weather data. By working with asynchronous programming and handling API responses with `async/await`, I ensured smooth data fetching and processing. I also gained hands-on experience in DOM manipulation, dynamically updating the user interface with weather details. Error handling was essential for providing clear messages when users entered invalid city names. Additionally, I became familiar with parsing JSON data, creating a responsive UI using CSS for both desktop and mobile devices, and using Git for version control. Handling user input efficiently and deploying the app on GitHub Pages helped me share my project with others. Overall, this project strengthened my skills in API integration, asynchronous JavaScript, DOM manipulation, and deployment, while enhancing my understanding of building interactive, user-friendly web applications.
## Screenshots

![This is the inter face of the App](![Image](https://github.com/user-attachments/assets/14e30e02-f673-4cb1-8368-df3754fe125b)
![When we search the city name in serch bar it give the tempeture, humabity and wind speed of that city](https://github.com/user-attachments/assets/9e5996ee-e117-4b5a-bab0-976015d315fa)
![When we apply wrong city name it will give invalid name ](https://github.com/user-attachments/assets/4cdcadb2-520d-41bd-b567-5a64a8cc2004)
![Image](https://github.com/user-attachments/assets/72bdd3e7-6473-4c27-aa1a-d667c9a0cebb)

