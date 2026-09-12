# 🌤️ Weather App

A simple and responsive **Weather App** built using **HTML, CSS, and JavaScript**. The application uses the **OpenWeatherMap API** to fetch real-time weather information for a city entered by the user.

## 🚀 Features

* 🔍 Search weather by city name
* 🌡️ Display current temperature
* 🏙️ Display city name
* 💧 Display humidity
* 💨 Display wind speed
* 🌤️ Dynamically change the weather icon based on weather conditions
* ❌ Display an error message for an invalid city
* 📱 Responsive layout
* ⚡ Fetch real-time weather data using the OpenWeatherMap API

## 🛠️ Technologies Used

* **HTML5** – Structure of the application
* **CSS3** – Styling, layout, and responsive design
* **JavaScript** – DOM manipulation, API requests, and application logic
* **OpenWeatherMap API** – Real-time weather data

## 📂 Project Structure

```text
Weather-App/
│
├── index.html
├── style.css
├── script.js
├── README.md
│
└── images/
    ├── clouds-and-sun.png
    ├── search.png
    ├── clouds.png
    ├── clear.png
    ├── drizzle.png
    ├── humidity.png
    ├── mist.png
    ├── rain.png
    └── wind.png
```

## ⚙️ How It Works

1. The user enters a city name in the search box.
2. JavaScript gets the entered city name from the input field.
3. A request is sent to the OpenWeatherMap API using `fetch()`.
4. The API returns the current weather information in JSON format.
5. JavaScript extracts the required information from the API response.
6. The weather information is dynamically displayed on the webpage.
7. The weather icon changes according to the current weather condition.
8. If the entered city is not found, an **"Invalid city name"** message is displayed.

## 🔌 API Integration

This project uses the **OpenWeatherMap Current Weather API**.

The API URL is configured in `script.js`:

```javascript
const apiUrl =
    "https://api.openweathermap.org/data/2.5/weather?units=metric&q=";
```

The `units=metric` parameter is used to receive temperature values in Celsius.

The application uses JavaScript's `fetch()` API along with `async/await` to retrieve weather data:

```javascript
const response = await fetch(
    apiUrl + city + `&appid=${apikey}`
);
```

The returned JSON data is then used to update the weather information on the webpage.

## 🌦️ Weather Conditions

The application dynamically changes the weather icon based on the weather condition returned by the API.

Currently supported conditions include:

* ☁️ Clouds
* ☀️ Clear
* 🌧️ Rain
* 🌦️ Drizzle
* 🌫️ Mist

Example:

```javascript
if (data.weather[0].main == "Clouds") {
    weatherIcon.src = "images/clouds.png";
}
else if (data.weather[0].main == "Clear") {
    weatherIcon.src = "images/clear.png";
}
else if (data.weather[0].main == "Rain") {
    weatherIcon.src = "images/rain.png";
}
```

## 💻 Running the Project

### 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Open the Project

Open the project folder in **VS Code**.

### 3. Run the Application

You can open `index.html` directly in your browser or use the **Live Server** extension in VS Code.

### 4. Search for a City

Enter a city name such as:

```text
Bengaluru
```

Then click the search button to view its current weather information.

## 🔐 API Key Security

The application currently uses the OpenWeatherMap API directly from frontend JavaScript.

This project is intended for **learning and portfolio purposes**. In a production application, API keys should not be exposed directly in client-side JavaScript.

A backend or server-side environment can be used to securely store the API key and make API requests.

## 📚 Concepts Practiced

This project helped practice several important web development and JavaScript concepts:

* HTML5
* CSS3
* CSS Flexbox
* Responsive Web Design
* JavaScript variables and constants
* JavaScript functions
* DOM manipulation
* `querySelector()`
* Event listeners
* `fetch()`
* REST API integration
* JSON data
* `async/await`
* Conditional statements
* Template literals
* HTTP status handling
* Dynamic content updates
* Dynamic image changes
* API integration

## 🔮 Future Improvements

Possible improvements for the project:

* 📍 Add weather based on the user's current location
* 📅 Add a 5-day weather forecast
* 🕐 Add an hourly weather forecast
* 🌅 Display sunrise and sunset times
* 🌡️ Display "feels like" temperature
* 🌧️ Display precipitation information
* 🌙 Add dark/light mode
* ⌨️ Search when pressing the **Enter** key
* 🌎 Display country information
* 📊 Display additional weather statistics
* 🔒 Move API requests to a backend for better API-key security

## 👨‍💻 Author

**Divakar**

A frontend project created to practice **HTML, CSS, JavaScript, API integration, DOM manipulation, and responsive web development**.
