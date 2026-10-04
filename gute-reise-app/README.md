# Gute Reise App - Smart Navigation with Auto-Refuel

Advanced navigation app that automatically inserts fuel / charging stops into the route based on vehicle profile.

### What it does
- Full navigation with OSM
- Vehicle profile: fuel type, consumption, tank size, EV battery, range
- Auto-calculates when refuel/charging is needed
- Automatically inserts best stations into the route
- Considers price, detour time, and plug compatibility

### Project Structure & Architecture
**Folder Structure (real):**
lib/
/models/ -> Vehicle, Route, Station models
/services/ -> Routing service, Tank API, Consumption algorithm
/screens/ -> Main map and route screens
/helpers/ -> Route calculation helpers
/widgets/ -> Map widgets, Station markers
/widgets/navigation/ -> Navigation UI
/widgets/navigation/sheets/ -> Bottom sheets for station selection


**Architecture: Hybrid Offline + Online**
1. Offline: Maps (OSM tiles) & Routing (GraphHopper) cached locally
2. Online: Live fuel prices & EV stations fetched via API
3. Core Logic: Consumption algorithm calculates when to insert stop
- Complex business logic, not just a map.

### Tech Stack
- Flutter / Dart / Isar DB (for route cache)
- OpenStreetMap + GraphHopper
- Tankerkoenig + OpenChargeMap API

> Full algorithm and architecture available privately for clients (NDA).
