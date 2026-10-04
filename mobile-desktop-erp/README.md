# MobileDesktopERP - Cross-Platform ERP | Android & Windows

Production-ready ERP built from **one Flutter codebase** for Android (mobile/warehouse) and Windows (desktop/office). Currently productive in use.

### Profile
**Florin G. - IHK Fachinformatiker für Anwendungsentwicklung**
Bochum, NRW | Remote & Vor-Ort | 550€/Tag

### Tech Stack
- **Framework:** Flutter 3.x / Dart
- **Database:** Isar DB (NoSQL, offline-first, fast)
- **State:** Provider + ChangeNotifier
- **Platform:** Android + Windows (one codebase, adaptive UI)
- **Sync:** Google Drive API (DSGVO-konform backup & sync)
- **Export:** PDF (pdf package), CSV
- **Arch:** Clean Architecture, Offline-First

### Key Features (What German clients pay for)

**1. 100% Offline-First - 60 Days without Internet**
App works fully offline in warehouse. All data in Isar DB. Syncs automatically when online via Google Drive. No data loss.

**2. One Codebase, Two Platforms**
- Android: optimized for scanner, touch, small screens
- Windows: optimized for keyboard, mouse, large tables, printers
- Same business logic, 90% shared code

**3. DSGVO-Konform**
No external cloud. Customer data stays in local Isar DB + own Google Drive. No US tracking.

**4. Real ERP Features**
- Artikel-, Kunden-, Auftragsverwaltung
- Barcode scanning (mobile)
- PDF Angebot / Rechnung export
- Lagerbestand in real-time

### Project Structure & Architecture
**Folder Structure (real):**
lib/
/models/ -> Isar collections (Product, Order, Customer)
/services/ -> Isar DB service, Google Drive Sync, PDF Export
/screen/ -> Shared screens
/screen/mobile/ -> Android-optimized UI (touch, scanner)
/screen/desktop/ -> Windows-optimized UI (keyboard, tables)
/widgets/ -> Reusable adaptive widgets


**Architecture: Offline-First + Platform-Adaptive**
1. UI (mobile/desktop) -> calls Service
2. Service -> reads/writes 100% from Isar DB (works offline 60 days)
3. Background Sync Service -> syncs Isar to Google Drive when online
- One business logic, two UIs from same codebase.

### Code Example - Isar Offline Service
```dart
// core/database_service.dart
class DatabaseService {
  late Isar isar;
  
  Future<void> init() async {
    isar = await Isar.open([ProductSchema, OrderSchema]);
  }

  // Works 100% offline
  Future<List<Order>> getOrders() => isar.orders.where().findAll();
}

Full source available privately for clients (NDA).
