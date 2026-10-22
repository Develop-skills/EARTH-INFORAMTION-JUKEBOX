# EARTH-INFORAMTION-JUKEBOX
A web application for exploring and discovering interactive Earth information and datasets.

# Branch out based on your role:
git checkout -b feature/fullstack-command   # Person 1
git checkout -b feature/data-ml-causal      # Person 2 & 3
git checkout -b feature/incident-agent      # Person 4 & 5
🌍 External Hazard Map Providers & API Keys
The application runs 100% out of the box with zero paid API keys, utilizing graceful web fallbacks and public government feeds. Optional keys can be placed in .env (refer to .env.example).

1. Windy Atmospheric Radar (Wind, Rain, Clouds, Waves)
Without API Key (Default): Displays the official https://embed.windy.com interactive viewport centered on Mumbai (19.076, 72.8777). Note: Iframe mode cannot synchronize with custom timeline scrubs.
With API Key: Set WINDY_MAP_API_KEY in .env to enable native Leaflet map integration per the Windy Map API Docs.
Get a Key: Register at https://api.windy.com/keys.
Required Attribution: Keep Wind & weather data: Windy.com visible on the map interface.
2. Google Flood Hub (Upstream Riverine Risk)
Without API Key (Default): The "Upstream river risk" layer opens an operator direct link to the Google Flood Hub Mumbai Portal.
With API Key: Set GOOGLE_FLOOD_API_KEY in .env to query the official Google Flood Forecasting API. Gauges are fetched server-side and cached for 15 minutes.
Request Access: Apply via Google Developers Flood Forecasting.
Important Note: Google Flood Hub models riverine flood risks, not street-level drainage/waterlogging.
Required Attribution: Flood forecast data: Google Flood Hub, CC BY 4.0.
3. USGS Earthquakes (Global & Mumbai Region)
Live Feed: Polled every 5 minutes from https://earthquake.usgs.gov/earthquakes/feed/v1.0/summary/2.5_day.geojson (no key required).
Demo Injection: Use the "🌋 Inject Earthquake (USGS Demo)" scenario button in the dashboard to simulate ground motion and test causal classification even when seismic activity is quiet.
Required Attribution: Earthquake data: USGS, public domain.
