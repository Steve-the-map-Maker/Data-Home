# Steve's Data & Mapping Portfolio

Welcome to my portfolio, where data and creativity come together to map the world in insightful ways. Through a mix of interactive dashboards and visualizations, I aim to shed light on stories hidden within the numbers—whether it's exploring election outcomes, demographic trends, or economic landscapes.

Each project you’ll find here is an attempt to bring clarity and context to complex topics through the lens of data. Feel free to explore the maps and analyses I’ve created, and discover how different communities and places can be understood more deeply through the power of visual data storytelling.

This repository contains the HTML, CSS, and data files for the portfolio website.

## Running the Portfolio Locally

This is a static website built with HTML, CSS, and JavaScript. To view it locally, you can use a simple local web server.

1.  Clone or download this repository.
2.  Navigate to the `Data-Home` directory in your terminal.
3.  If you have Python 3, you can run a simple web server:
    ```bash
    python -m http.server
    ```
4.  Open your web browser and go to `http://localhost:8000` to see the `index.html` page.

## Projects

Here is a summary of the projects featured in this portfolio.

---

### 1. Pickleball Courts Map

An interactive web application designed to help users discover pickleball court locations in the Portland area. This map provides a dynamic visualization of court data and offers various filtering options to enhance your search.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More

#### Key Features

*   **Interactive Map Display:** Visualizes pickleball courts on a dynamic MapLibre map.
*   **Geolocation:** Allows users to find courts near their current location.
*   **Advanced Filtering:**
    *   Filter courts by distance from the user (1km to 100km).
    *   Filter by court type (Indoor, Outdoor, or Any).
    *   Filter by the minimum number of courts available at a location (1 to 8+).
*   **Dynamic Sidebar:**
    *   Lists courts based on the current map view and active filters.
    *   Displays detailed information for a selected court in a slide-in panel.
*   **"Get Directions":** Provides a link to Google Maps for directions to the selected court.
*   **Dynamic Map Marker Styling:** Markers are styled based on the number of courts and court type.
*   **Responsive Design:** Adapts to different screen sizes.

#### Technology Stack

*   **Frontend:** HTML5, CSS3, JavaScript (ES6+)
*   **Mapping Library:** MapLibre GL JS
*   **Basemap:** OpenStreetMap
*   **Data Format:** GeoJSON

---

### 2. Census AI Data Visualizer

An AI-powered tool for natural language queries and visualizations of U.S. Census data. This full-stack application uses a Python backend with Google Gemini Pro to interpret user queries and a React frontend to display the results on an interactive map.

*   **Live Application:** View App
*   **Project Details Page:** Learn More

---

### 3. Fantasy Football App

A React.js application for analyzing fantasy football player data and performance. It features interactive tables, player cards, and charts to visualize player performance and rankings.

*   **Live Application:** View App
*   **Project Details Page:** Learn More

---

### 4. Election Forecast Model

A machine learning model predicting voter turnout and candidate support across precincts for the Portland mayoral race. This project uses a Gradient Boosting Regressor and historical election data to make its forecasts.

*   **Project Details Page:** Learn More

---

### 5. DA Results (Vasquez vs Schmidt 2024)

A web dashboard showing the election results by precinct for Portland's DA race. The map visualizes vote percentages and support levels across different districts.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More

---

### 6. LA & Orange County Income Map

An interactive map to explore the median income of Los Angeles and Orange County per census tract, built with React and MapLibre.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More

---

### 7. Portland By Age

An interactive dashboard to explore the age demographic distribution across Portland using U.S. Census data.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More

---

### 8. Portland City Council Election Results (2022)

This web dashboard shows the election results by precinct in Portland for the 2022 city council race between Rene Gonzalas and JoAnn Hardesty.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More


*   **Live Application:** [View App](https://census-ai-frontend.onrender.com/)
*   **Project Details Page:** [Learn More](CensusAIDetails.html)

#### Key Features

*   **Natural Language Querying:** Allows users to ask questions about census data in plain English (e.g., "Show me the median income in Portland, Oregon").
*   **AI-Powered Backend:** Utilizes Google Gemini Pro to parse queries, identify relevant data points, and generate visualizations.
*   **Interactive Map Display:** Presents data on a dynamic map, allowing for exploration of geographical patterns.
*   **Full-Stack Architecture:** A modern web application with a clear separation between the frontend logic and the backend AI processing.

#### Technology Stack

*   **Frontend:** React, MapLibre GL JS
*   **Backend:** Python
*   **AI/ML:** Google Gemini Pro API
*   **Data Source:** U.S. Census Bureau API

---

### 3. Fantasy Football App

A React.js application for analyzing fantasy football player data and performance. It features interactive tables, player cards, and charts to visualize player performance and rankings.

*   **Live Application:** View App
*   **Project Details Page:** Learn More
*   **Live Application:** [View App](https://Steve-the-map-Maker.github.io/fantasy-football-app)
*   **Project Details Page:** [Learn More](FantasyFootballAppDetails.html)

#### Key Features

*   **Interactive Data Tables:** Sortable and filterable tables of player statistics.
*   **Detailed Player Cards:** In-depth view of individual player performance and metrics.
*   **Performance Charts:** Visualizations to compare players and track trends over time.
*   **Data-Driven Analysis:** Provides tools for fantasy football drafts and weekly matchup decisions.

#### Technology Stack

*   **Frontend:** React.js, HTML5, CSS3
*   **Data Visualization:** Charting libraries
*   **Data Source:** Fantasy football data API or static data files

---

### 4. Election Forecast Model

A machine learning model predicting voter turnout and candidate support across precincts for the Portland mayoral race. This project uses a Gradient Boosting Regressor and historical election data to make its forecasts.

*   **Project Details Page:** Learn More
*   **Project Details Page:** [Learn More](ElectionModel.html)

#### Key Features

*   **Predictive Modeling:** Forecasts precinct-level voter turnout and candidate support using a `GradientBoostingRegressor`.
*   **Rich Feature Set:** Incorporates historical data from multiple past elections (mayoral, DA, metro measures) to improve accuracy.
*   **Model Interpretability:** Uses SHAP (SHapley Additive exPlanations) to explain the impact of each feature on the model's predictions.
*   **Feature Importance Analysis:** Identifies the most influential factors driving election outcomes.
*   **Detailed Results:** Presents predictions in an interactive table with forecasted vote counts and SHAP-based interpretations.

#### Technology Stack

*   **Modeling & Analysis:** Python, Pandas, Scikit-learn, SHAP
*   **Frontend Display:** HTML5, CSS3, JavaScript, PapaParse

---

### 5. DA Results (Vasquez vs Schmidt 2024)

A web dashboard showing the election results by precinct for Portland's DA race. The map visualizes vote percentages and support levels across different districts.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More
*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More

#### Key Features

*   **Precinct-Level Visualization:** Displays election results on an interactive MapLibre map.
*   **Choropleth & Opacity Styling:** Uses a color gradient for vote percentage and transparency for normalized vote count (turnout).
*   **District Overlays:** Highlights commissioner district boundaries for regional analysis.
*   **Interactive Filtering:** A toggle allows users to switch between the full county view and a focus on the City of Portland.

#### Technology Stack

*   **Frontend:** HTML5, CSS3, JavaScript
*   **Mapping Library:** MapLibre GL JS
*   **Basemap:** OpenStreetMap
*   **Data Format:** GeoJSON

---

### 6. LA & Orange County Income Map

An interactive map to explore the median income of Los Angeles and Orange County per census tract, built with React and MapLibre.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More
*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More

#### Key Features

*   **Census Tract Visualization:** Maps the median household income for every census tract in Los Angeles and Orange County.
*   **Interactive Choropleth Map:** Uses a color scale to represent different income brackets, making it easy to spot geographic trends.
*   **Tooltip Information:** Hovering over a census tract displays its specific median income.

#### Technology Stack

*   **Frontend:** React, MapLibre GL JS, HTML5, CSS3
*   **Data Source:** U.S. Census Bureau

---

### 7. Portland By Age

An interactive dashboard to explore the age demographic distribution across Portland using U.S. Census data.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More
*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More

#### Key Features

*   **Multi-faceted Dashboard:** Combines an interactive map, a bar chart, and a pie chart for a comprehensive view of age demographics.
*   **Spatial Distribution Map:** Visualizes the median age by census tract across Portland.
*   **Statistical Charts:** Includes a bar chart of tracts per age group and a pie chart of the total population distribution.

#### Technology Stack

*   **Frontend:** HTML5, CSS3, JavaScript
*   **Mapping Library:** MapLibre GL JS
*   **Data Source:** U.S. Census Bureau

---

### 8. Portland City Council Election Results (2022)

This web dashboard shows the election results by precinct in Portland for the 2022 city council race between Rene Gonzalas and JoAnn Hardesty.

*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More
*   **Live Application:** View Dashboard
*   **Project Details Page:** Learn More

#### Key Features

*   **Precinct-Level Visualization:** Displays 2022 City Council election results on an interactive map.
*   **Choropleth Styling:** Uses color to represent the winner or vote share in each precinct.
*   **Interactive Tooltips:** Hovering over a precinct shows detailed vote counts for each candidate.

#### Technology Stack

*   **Frontend:** HTML5, CSS3, JavaScript
*   **Mapping Library:** MapLibre GL JS
*   **Basemap:** OpenStreetMap
*   **Data Format:** GeoJSON

