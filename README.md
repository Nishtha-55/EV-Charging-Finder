
# ⚡ EV Charging Finder (Prototype)

A single-file web prototype that shows how EV Charging Finder works: type a city,
road or landmark, and it finds the nearest charging station and draws a route map.

Built as a B.Tech CSE mini project at Kanpur Institute of Technology, Kanpur.

## Features
- Place-name search, or direct coordinates such as `26.45, 80.33`
- Nearest-station selection by geodesic distance
- Schematic SVG map with markers and an illustrative route line
- Pages: Home, Finder, Stations, Saved, About (hash navigation)
- Local storage: search history, favourite stations, added stations, last result
- Add and remove your own stations
- Grey and turquoise theme, with automatic dark mode

## Run it
Download `index.html` and open it in any modern browser. No install or server needed.

## How it relates to the original project
This prototype follows the workflow of the original Python project
(place name → geocoding → station search → route → map), but replaces the
online services so it runs fully offline.

| Stage | Original | This prototype |
|---|---|---|
| Geocoding | geopy + Nominatim | Built-in city list or lat, lon |
| Stations | Bundled CSV | Sample rows plus your additions |
| Distance | geopy geodesic | Haversine formula |
| Route | OSRM | Illustrative curve |
| Map | Folium / Leaflet | Inline SVG |

## Limitations
- Station data is sample data, not verified real chargers
- Only the nearest station is returned
- No live availability, pricing or connector information
- Straight-line distance is not road distance

## Credits
Based on the public [EV-Charging-Finder](https://github.com/sonubiswal/EV-Charging-Finder)
repository by Sonu Biswal. The original source, dataset and external services are
acknowledged and are not claimed as original work. This prototype is a separate
study implementation.

## Author
Nishtha Srivastava · B.Tech CSE-B · Kanpur Institute of Technology, Kanpur
