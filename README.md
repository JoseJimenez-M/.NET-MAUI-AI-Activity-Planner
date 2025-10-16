# PLAN-IT: AI-POWERED ACTIVITY SUGGESTIONS
## (Formerly Face&Fun)

Plan-It is an innovative mobile application (iOS/Android) built with .NET MAUI that transforms a simple photo into a fully personalized activity recommendation. It uses artificial intelligence to analyze the context of your environment and your preferences, suggesting the perfect plan for you and your company.

---

### 💡 KEY FEATURES

* **AI Face Detection:** Automatically determines the number of people in a photo for group or individual suggestions.
* **Intelligent Context:** Integrates real-time weather and location data.
* **Deep Personalization:** Filters suggestions by Romantic Mode, Budget Limit, Distance Range, and Activity Type (e.g., restaurant, picnic, art, action-based).
* **Suggestion Engine:** Combines all inputs to generate a unique keyword and queries place APIs for a high-quality recommendation.

---

### 🛠️ TECHNOLOGIES USED

* **Framework:** .NET MAUI (Native cross-platform development)
* **Face Detection:** UltraFaceDotNet (AI model for image analysis)
* **Service APIs:**
    * OpenWeatherMap: Current weather data.
    * Geoapify / Foursquare Places API: Location-based search and reverse geocoding.
* **Utilities:** Newtonsoft.Json (JSON parsing), MAUI Essentials (Native hardware/service access).

---

### ⚙️ PROJECT SETUP

#### Requirements
1.  Visual Studio 2022+ with the .NET MAUI workload installed.
2.  API Keys for external services.

#### API Keys
This application requires access to weather and location data.

1.  Obtain your API keys for:
    * OpenWeatherMap (Weather Data)
    * Geoapify (Reverse Geocoding / Location)
2.  Create a new file in your project: Resources/Raw/apikey.txt.
3.  Paste your keys into the file, each on a separate line, in the following order:

    YOUR_APIKEY_OPENWEATHER
    YOUR_APIKEY_GEOAPIFY

    *Security Note: The apikey.txt file is already included in .gitignore to prevent your credentials from being accidentally uploaded to the repository.*

#### Running the App
1.  Open the project in Visual Studio 2022+.
2.  Ensure the apikey.txt file is correctly configured in Resources/Raw/.
3.  Select your target platform (Android/iOS) and run the application.
4.  Upon first launch, you will need to grant permissions for camera, location, and storage when prompted.

---

### 🧑‍💻 HOW THE APP WORKS (WORKFLOW)

1.  **Start:** The app automatically fetches your location and the current weather.
2.  **Input:** The user takes a photo, and the AI detects the number of faces.
3.  **Preferences:** The user adjusts key filters:
    * Romantic Mode (On/Off)
    * Budget Limit (€ / $)
    * Distance Range (km)
    * Activity Type (Restaurant, Walk, Picnic, etc.)
4.  **Suggestion:** The system generates a keyword and queries the Foursquare Places API using location, distance, and filters.
