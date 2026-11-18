# 🌍 Context-Aware Geospatial Query System

<p align="center">
  <strong>An AI-driven system for retrieving and visualizing geographical information through context-aware natural language queries.</strong>
</p>

---

## 📌 Project Overview

The Context-Aware Geospatial Query System is a Python-based web application developed using Flask that integrates Artificial Intelligence (AI) with Geographic Information Systems (GIS) to simplify geographical information retrieval through natural language queries.

The system leverages Google's Gemini API to interpret user queries, identify their intent, and retrieve relevant location-based information through geospatial APIs. It supports context-aware query processing, allowing users to ask follow-up questions based on previous interactions.

The application integrates OpenStreetMap Nominatim for geocoding, OpenRouteService for route generation and distance calculation, and OpenStreetMap Overpass API for retrieving nearby Points of Interest (POIs).

Retrieved geographical information, including locations, routes, and nearby facilities, is presented through an interactive map interface. Additionally, SQLite is used to maintain conversational query history, enabling a lightweight and context-aware geospatial information retrieval experience.

The system aims to bridge the gap between conventional geographical information systems and conversational AI by making location-based information more accessible through natural language interactions.

## 🎯 Objectives

- Develop an intelligent conversational interface for retrieving geospatial information.
- Integrate AI-based natural language processing for query classification and interpretation.
- Implement context-aware query processing to support conversational follow-up interactions.
- Retrieve geographical information using external geospatial APIs.
- Identify nearby Points of Interest based on geographical location and search radius.
- Generate routes and calculate distances between geographical locations.
- Integrate weather and timezone information into location-based responses.
- Visualize geographical results through an interactive map interface.

## ✨ Key Features

### 1. Context-Aware Natural Language Processing

- Uses Google Gemini API to interpret natural-language geospatial queries.
- Classifies user queries based on their intent and information requirements.
- Maintains conversational context to process follow-up questions.
- Generates contextual and user-friendly responses.

### 2. Geocoding and Location Retrieval

- Uses OpenStreetMap Nominatim for forward and reverse geocoding.
- Retrieves geographical coordinates and location-specific information.
- Provides contextual information about identified locations.
- Retrieves weather conditions and local timezone information.

### 3. Points of Interest (POI) Retrieval

- Identifies nearby facilities based on a specified geographical location.
- Retrieves categories such as restaurants, hospitals, schools, parks, ATMs, pharmacies, banks, and other facilities.
- Supports location-based searches with configurable search radius.
- Uses OpenStreetMap Overpass API to retrieve nearby geographical entities.

### 4. Route Generation and Distance Calculation

- Integrates OpenRouteService API to generate routes between geographical locations.
- Supports driving, cycling, and walking routes.
- Retrieves route distances and navigation instructions.
- Provides route information through geographical coordinates.

### 5. Interactive Geospatial Visualization

- Visualizes geographical locations, routes, and nearby Points of Interest.
- Displays location markers with relevant geographical information.
- Presents route information through an interactive map interface.

### 6. Weather and Timezone Information

- Retrieves location-based weather information using OpenWeatherMap.
- Provides temperature, wind speed, and weather conditions.
- Identifies the local timezone and corresponding local time.

### 7. Conversational Context and History

- Uses Flask sessions to maintain conversational context.
- Stores user queries and generated responses using SQLite.
- Supports context-aware follow-up interactions.
- Maintains a lightweight conversational history for the application.

## 🛠️ Technology Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Backend Framework | Flask |
| Artificial Intelligence | Google Gemini 1.5 Flash |
| Geocoding | Geopy, OpenStreetMap Nominatim |
| Routing | OpenRouteService API |
| Points of Interest | OpenStreetMap Overpass API, Overpy |
| Weather Information | OpenWeatherMap API |
| Timezone Detection | TimezoneFinder, pytz |
| Database | SQLite |
| HTTP Requests | Requests |
| Deployment | Gunicorn |

## 🏗️ System Architecture

The application follows an AI-driven request-processing architecture:

1. **User Query:** The user submits a geographical query through the application interface.
2. **Query Processing:** Flask receives the request and forwards it for processing.
3. **AI Interpretation:** Google Gemini AI identifies the intent and category of the query.
4. **Context Management:** Previous conversational interactions are considered when processing follow-up questions.
5. **API Integration:** The application communicates with the appropriate external geospatial services.
6. **Data Retrieval:** Relevant geographical, routing, weather, or location information is retrieved.
7. **Response Generation:** Retrieved information is processed into contextual, user-friendly responses.
8. **Map Visualization:** Geographical results are returned to the frontend for visualization.
9. **History Management:** Conversational information is maintained using Flask sessions and SQLite.

## 🌐 External APIs and Services

| API / Service | Purpose |
|---|---|
| Google Gemini API | Natural language understanding, query classification, and response generation |
| OpenStreetMap Nominatim | Forward and reverse geocoding |
| OpenRouteService API | Route calculation, distance retrieval, and navigation instructions |
| OpenStreetMap Overpass API | Retrieval of nearby Points of Interest |
| OpenWeatherMap API | Weather information based on geographical coordinates |

## 📂 Project Structure

```text

AI-Geospatial-main/
│
├── templates/
│   └── map1_1.html
│
├── venv/
│   ├── Include/
│   ├── Lib/
│   ├── Scripts/
│   └── pyvenv.cfg
│
├── .gitignore
├── geo_chat_history.db
├── main3.py
├── Procfile
├── README.md
└── requirements.txt
```

## ⚙️ Installation and Setup

### Prerequisites

Ensure that the following are installed:

- Python 3
- Git
- Google Gemini API key
- OpenRouteService API key
- OpenWeatherMap API key

### 1. Clone the Repository

```bash
git clone https://github.com/ShreyasK95/Context_Aware_geospatial.git
```

### 2. Navigate to the Project Directory

```bash
cd Context_Aware_geospatial
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate the Virtual Environment

**Windows (PowerShell):**

```powershell
.\venv\Scripts\Activate.ps1
```

**Linux / macOS:**

```bash
source venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Configure API Credentials

Obtain the required API credentials from the respective service providers.

Configure the following environment variables:

```env
GOOGLE_API_KEY=your_google_gemini_api_key
ORS_API_KEY=your_openrouteservice_api_key
OWM_API_KEY=your_openweathermap_api_key
```

Store these credentials in a local `.env` file or configure them as system environment variables.

Ensure that the application reads the credentials securely through environment variables.

**Important:** Never commit API credentials, passwords, or `.env` files to GitHub.

### 7. Run the Application

```bash
python main3.py
```

The Flask application runs on port `10000`.

Open your browser and navigate to:

```text
http://localhost:10000
```

## 🗄️ Database

The application uses SQLite to maintain conversational history.

The `geo_chat_history.db` database is initialized automatically when the application starts. It stores user queries and their corresponding chatbot responses.

The database is generated locally and does not need to be included in the GitHub repository.

## 🚀 Future Enhancements

- Improve AI-based query classification and geographical entity extraction.
- Expand support for additional geographical datasets and location categories.
- Enhance interactive map visualization and user experience.
- Introduce advanced spatial analysis and geospatial data processing.
- Improve conversational memory and context management.
- Strengthen API error handling and application performance.
- Introduce additional location-based analytical capabilities.

## 🙏 Acknowledgements

We acknowledge the following platforms, technologies, and services for supporting the development of this project:

- [Google Gemini](https://ai.google.dev/)
- [OpenStreetMap](https://www.openstreetmap.org/)
- [OpenRouteService](https://openrouteservice.org/)
- [OpenWeatherMap](https://openweathermap.org/)
- [Flask](https://flask.palletsprojects.com/)
- [Geopy](https://geopy.readthedocs.io/)

---

<p align="center">
  <strong>Context-Aware Geospatial Query System – Bridging Conversational AI and Geospatial Information Retrieval.</strong>
</p>