# Source Code Extractor - WinUI 3 | Microsoft Store Published

Windows productivity tool for developers. Full offline, published live in Microsoft Store.

### What it does
- Extracts and merges source code from Visual Studio projects
- Cleans up /bundles code for sharing or AI prompts
- 100% offline, no cloud, no tracking - DSGVO-konform

### Project Structure & Architecture

**Folder Structure (real - WinUI 3 / MVVM):**
/Assets/ -> App icons, Store assets
/Imgs/ -> UI images
/Themes/ -> WinUI styles
/Models/ -> File extraction logic, Project models
/ViewModels/ -> MVVM ViewModels (business logic)
/Views/ -> WinUI 3 XAML Views
/Commands/ -> ICommand implementations


**Architecture: MVVM + 100% Offline**
1. Views (WinUI XAML) <-> ViewModels (MVVM)
2. ViewModels -> Models (file system access via Windows.Storage)
3. No internet needed. All processing local.
- End-to-end delivery: Dev -> MSIX packaging -> Store publishing.

### Tech Stack
- C# / .NET / WinUI 3
- MVVM Pattern
- Windows App SDK / MSIX
- Microsoft Store Deployment (Store listing, certification)

### Link
**Microsoft Store:** https://apps.microsoft.com/detail/9NM2CZS5BBH1?hl=en-us&gl=DE&ocid=pdpshare

### Key Feature for Clients
Proves I can deliver a full Windows product: from code to Store. Not just coding, but publishing, certification and lifecycle.

> Full source available privately for clients (NDA).
