# exitFy V2 (Fixed for modern exteraless & AyuGram)

Optimized Telegram proxy and connection acceleration plugin.

### Key Fixes in this Release:
- **Fixed Infinite Connecting:** Implemented modern Telegram `ProxySettings` bridge and compatibility fallback so proxy settings attach cleanly to the native connection manager without hanging on *"Connecting..."*.
- **Full exteraless Sandbox Support:** Explicitly declared `__permissions__` (`network`, `files`, `hooks`, `native`, `settings`, `messages.send`) so exteraless grants necessary capabilities on install without permission errors.
- **AyuGram & AyuGram FCMWeb Compatibility:** Added safe reflective resolution for `ConnectionsManager` across all Telegram/AyuGram package variants (`org.telegram.messenger`, `org.telegram.messenger.web`).

### Installation:
1. Download `exitFy_v2.plugin`.
2. Send it to your Saved Messages or open it with **exteraless** / **AyuGram** / **exteraGram**.
3. Tap on the plugin file and click **Install**.
4. Grant the requested permissions.
5. In the plugin settings, tap **Install components** (Установить компоненты), select your provider (e.g. *Shrimp*), and tap **Connect**.
