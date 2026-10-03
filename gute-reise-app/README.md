# Gute Reise App - Smart Navigation with Auto-Refuel

Advanced navigation app that automatically inserts fuel / charging stops into the route based on vehicle profile.

### What it does
- Full navigation with OSM
- Vehicle profile: fuel type, consumption, tank size, EV battery, range
- Auto-calculates when refuel/charging is needed
- Automatically inserts best stations into the route
- Considers price, detour time, and plug compatibility
- Offline maps and route caching

### Tech Stack
- Flutter / Dart / Isar DB (offline-first)
- OpenStreetMap + Routing Engine (OSRM / GraphHopper)
- Tankpreis + EV APIs
- Complex business logic: consumption algorithm

### Key Feature for Clients
This is NOT a simple map app. This is business logic + navigation + offline-first. 
Shows ability to build complex, real-world products from scratch.

> Architecture and core algorithm available privately for clients.
