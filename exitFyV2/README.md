# exitFy V2 (Fixed for modern exteraless, AyuGram & ISP Mirror Fix)

Optimized Telegram proxy and connection acceleration plugin.

### Key Fixes in this Release:
- **Fixed Infinite Connecting:** Implemented modern Telegram `ProxySettings` bridge and compatibility fallback so proxy settings attach cleanly to the native connection manager without hanging on *"Connecting..."*.
- **Full exteraless Sandbox Support:** Explicitly declared `__permissions__` (`network`, `files`, `hooks`, `native`, `settings`, `messages.send`) so exteraless grants necessary capabilities on install without permission errors.
- **AyuGram & AyuGram FCMWeb Compatibility:** Added safe reflective resolution for `ConnectionsManager` across all Telegram/AyuGram package variants (`org.telegram.messenger`, `org.telegram.messenger.web`).
- **Restricted / Blocked ISP 44% Fix (Direct Component Hosting):** 
  - The native Sing-box (`libexitfy-sb-arm64-v8a.so`) and Xray (`libxray-arm64-v8a.so`) cores and manifests are hosted directly inside this repository under `exitFyV2/components/`.
  - Added an automated multi-mirror downloader (raw GitHub, Fastly jsDelivr, GitMirror, GHProxy) in Python that verifies hashes and pre-installs the cores before Java DEX initiates the download, preventing downloads from stalling or timing out at 44%.
  - Added a manual **"📥 Установить компоненты (Зеркало)"** item in the drawer menu for one-tap component installation / repair.

### Components Hosted in Repository:
- **Sing-box Core:** `exitFyV2/components/sing-box/libexitfy-sb-arm64-v8a.so` (version `sb-v1.14.3-w1001132`, ABI `arm64-v8a`)
- **Xray Core:** `exitFyV2/components/xray/libxray-arm64-v8a.so` (version `xray-v26.10.21-w1078`, ABI `arm64-v8a`)
- Manifests and detached cryptographic signatures (`manifest.json`, `manifest.json.sig`).

### Installation:
1. Download `exitFy_v2.plugin`.
2. Send it to your Saved Messages or open it with **exteraless** / **AyuGram** / **exteraGram**.
3. Tap on the plugin file and click **Install**.
4. Grant the requested permissions.
5. In the drawer menu, tap **"📥 Установить компоненты (Зеркало)"** or open plugin settings -> **Установить компоненты**, select your provider (e.g. *Shrimp*), and tap **Connect**.
