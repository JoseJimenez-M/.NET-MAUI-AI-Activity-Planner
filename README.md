Plan-It: AI-Powered Activity Suggestions 🚀
(Formerly Face&Fun)
Plan-It is an innovative mobile application (iOS/Android) built with .NET MAUI that transforms a simple photo into a fully personalized activity recommendation. It uses artificial intelligence to analyze the context of your environment and your preferences, suggesting the perfect plan for you and your company.

💡 Key Features
AI Face Detection: Automatically determines the number of people in a photo for group or individual suggestions.

Intelligent Context: Integrates real-time weather ☁️ and location 📍 data.

Deep Personalization: Filters suggestions by Romantic Mode, Budget Limit, Distance Range, and Activity Type (e.g., restaurant, picnic, art, action-based).

Suggestion Engine: Combines all inputs to generate a unique keyword and queries place APIs for a high-quality recommendation.

🛠️ Technologies Used
Framework: .NET MAUI (Native cross-platform development)

Face Detection: UltraFaceDotNet (AI model for image analysis)

Service APIs:

OpenWeatherMap: Current weather data.

Geoapify / Foursquare Places API: Location-based search and reverse geocoding.

Utilities: Newtonsoft.Json (JSON parsing), MAUI Essentials (Native hardware/service access).

⚙️ Project Setup
Requirements
Visual Studio 2022+ with the .NET MAUI workload installed.

API Keys for external services.

API Keys 🔑
This application requires access to weather and location data.

Obtain your API keys for:

OpenWeatherMap (Weather Data)

Geoapify (Reverse Geocoding / Location)

Create a new file in your project: Resources/Raw/apikey.txt.

Paste your keys into the file, each on a separate line, in the following order:

Plaintext

YOUR_APIKEY_OPENWEATHER
YOUR_APIKEY_GEOAPIFY
Security Note: The apikey.txt file is already included in .gitignore to prevent your credentials from being accidentally uploaded to the repository.

Running the App
Open the project in Visual Studio 2022+.

Ensure the apikey.txt file is correctly configured in Resources/Raw/.

Select your target platform (Android/iOS) and run the application.

Upon first launch, you will need to grant permissions for camera, location, and storage when prompted.

🧑‍💻 How the App Works (Workflow)
Start: The app automatically fetches your location and the current weather.

Input: The user takes a photo 📸, and the AI detects the number of faces.

Preferences: The user adjusts key filters:

Romantic Mode (On/Off)

Budget Limit (€ / $)

Distance Range (km)

Activity Type (Restaurant, Walk, Picnic, etc.)

Suggestion: The system generates a keyword and queries the Foursquare Places API using location, distance, and filters.

Result: A recommended activity is displayed with its Name, Category, Address, and Image (if available).
