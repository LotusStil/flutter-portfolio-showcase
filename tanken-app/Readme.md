# Tanken App - Nearby Fuel & EV Stations

Simple and fast Flutter app to find fuel stations and EV charging nearby. Clean MVP architecture.

### What it does
- Finds stations within ~10 km radius (GPS)
- Shows stations on OpenStreetMap + bottom sliding list (map <-> list sync)
- For fuel: shows live prices (Diesel, Benzin, E10)
- For EV: shows plug types (CCS, Type2, CHAdeMO)
- On tap -> Opens Google Maps for navigation

### Project Structure & Architecture

**Folder Structure (real - Simple MVP):**
lib/
main.dart -> App entry
map_page.dart -> Main page: Map + Sliding List logic
/components/
fuel_tile.dart -> Fuel station list item
charger_tile.dart -> EV station list item
detail_overlay.dart -> Station details on map tap
widgets.dart -> Shared small widgets


**Architecture: Online-First + Lean MVP**
1. `map_page.dart` gets GPS -> calls Tankerkoenig / OpenChargeMap API
2. API response -> renders markers on OSM + tiles in list
3. No local DB needed, just in-memory cache (fast, simple)
- Goal: Deliver working product in days, not weeks.

### Tech Stack
- Flutter / Dart
- OpenStreetMap (flutter_map)
- Tankerkoenig API / OpenChargeMap API
- Google Maps intent for navigation

### Key Feature for Clients
Shows I can build a clean, fast MVP with API + Map integration without over-engineering. Perfect for PoC.

> Full code available privately on request.
