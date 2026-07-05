# DTimestamp Overlay — Chrome Web Store Test Instructions

## Overview

DTimestamp Overlay requires **no login, no account, and no authentication** of any kind.
All features are fully available immediately after installation with zero setup required.
No data leaves the browser. No network requests are made. Settings are stored locally
via chrome.storage.sync only.

---

## Quick Start (30 seconds)

1. Install the extension from the Chrome Web Store
2. Navigate to any http or https webpage (e.g. https://google.com)
3. A live date · time · timezone stamp appears immediately in the bottom-right corner
4. Click the extension icon in the toolbar to open the settings panel

---

## Core Feature Verification

### 1. Live Overlay on Pages

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open any website (e.g. https://www.google.com) | Overlay stamp appears bottom-right showing current date, time and timezone |
| 2 | Open a second tab (e.g. https://github.com) | Overlay appears on this tab too — works on every page |
| 3 | Wait 1 second | Time updates every second in real time |
| 4 | Switch between tabs | Overlay shows on each tab independently |

### 2. Settings Panel

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Click the DTimestamp icon in the Chrome toolbar | Settings popup opens |
| 2 | Observe the header area | "DTimestamp Overlay" title with ON/OFF toggle in top right |
| 3 | Observe the "LIVE PREVIEW" section | Mini viewport showing stamp positioned per current settings |
| 4 | Scroll down | Time, Hover to Hide, Layout, Appearance, Date Format, Timezone, Font sections visible |

### 3. ON/OFF Toggle

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | In the popup header, toggle the switch OFF | Overlay disappears from the page immediately |
| 2 | Check the Live Preview in popup | Preview stamp disappears; "⏸ Overlay is off" message shown |
| 3 | Toggle back ON | Overlay reappears on the page; preview stamp returns |

### 4. Layout — Number of Lines

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup → Layout section | Three pills: 1 Line, 2 Lines, 3 Lines |
| 2 | Select "1 Line" | Overlay shows: `06-Jul-2026 · 10:30:45 AM · PDT` (all inline) |
| 3 | Select "2 Lines" | Overlay shows date on line 1, time + TZ on line 2 |
| 4 | Select "3 Lines" | Overlay shows date, time, timezone each on separate lines |
| 5 | Check Live Preview | Preview updates immediately to reflect line layout change |

### 5. Hover to Hide

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Ensure "Hide overlay when mouse hovers over it" is checked (on by default) | — |
| 2 | On any webpage, move cursor directly over the overlay stamp | Overlay fades out smoothly |
| 3 | Keep cursor over the overlay area | Overlay stays hidden |
| 4 | Move cursor away from overlay area | Countdown begins; after 5 seconds overlay fades back in |
| 5 | In popup, adjust "Re-show after cursor leaves" slider | Change delay (1–30 seconds), verify new delay on page |
| 6 | Uncheck "Hide overlay when mouse hovers over it" | Overlay no longer hides on hover |

### 6. Position

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup → Appearance → Position dropdown | 7 options shown |
| 2 | Select "Top Left" | Overlay moves to top-left of page; Live Preview stamp moves to top-left of mini viewport |
| 3 | Select "Center Screen" | Overlay appears in center of page; preview shows center position |
| 4 | Select "Bottom Right" | Returns to default position |
| 5 | Check each of the 7 positions | All move overlay correctly: Top Left, Top Center, Top Right, Bottom Left, Bottom Center, Bottom Right, Center Screen |

### 7. Theme

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup → Appearance → Theme | Options: Dark, Light, Blue, Green |
| 2 | Select "Dark" | Overlay changes to dark background, white text |
| 3 | Select "Light" | Overlay changes to white/light background, dark text |
| 4 | Select "Green" | Overlay changes to dark green background, green text |
| 5 | Select "Blue" (default) | Returns to default blue theme |

### 8. Date Format

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup → Date Format | Three options in dropdown |
| 2 | Select "DD-MON-YYYY" | Overlay shows e.g. `06-Jul-2026` |
| 3 | Select "DD/MM/YYYY" | Overlay shows e.g. `06/07/2026` |
| 4 | Select "MM/DD/YYYY" | Overlay shows e.g. `07/06/2026` |

### 9. Timezone

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup → Timezone → Select timezone | Dropdown with 25+ timezone presets |
| 2 | Select "UTC" | Overlay time changes to UTC |
| 3 | Select "Asia/Tokyo" | Overlay time changes to Japan Standard Time (JST) |
| 4 | Select "Local (your browser)" | Reverts to system/browser timezone |
| 5 | Change Label Format to "Long" | Overlay shows e.g. `JST · Asia/Tokyo` |
| 6 | Change Label Format to "Short" | Overlay shows e.g. `JST` only |

### 10. Font Customisation

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup → Font → Style | Four options: Mono, Sans, Serif, Rounded |
| 2 | Select each font style | Overlay text font changes accordingly; Live Preview updates |
| 3 | Font → Weight | Select Light through Bold — overlay weight changes |
| 4 | Font → Size slider | Drag from 10px to 22px — overlay text grows/shrinks |
| 5 | Font → Brightness slider | Lower to 40% — overlay text dims |
| 6 | Font → Opacity slider | Lower to 20% — overlay text becomes more transparent |

### 11. Background Opacity

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup → Appearance → Background opacity | Slider from 30% to 100% |
| 2 | Drag to 30% (minimum) | Overlay background is nearly transparent; text still visible |
| 3 | Drag to 100% | Overlay background is fully opaque |

### 12. Time Format

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup → Time → uncheck "Show seconds" | Overlay time shows HH:MM only, seconds hidden |
| 2 | Re-check "Show seconds" | Seconds reappear |
| 3 | Uncheck "AM/PM" | Switches to 24-hour format (e.g. `14:30:05`) |
| 4 | Re-check "AM/PM" | Returns to 12-hour format |

### 13. Settings Persistence

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Set a non-default position (e.g. Top Center) and theme (Dark) | Changes applied to overlay |
| 2 | Close Chrome completely | — |
| 3 | Reopen Chrome and visit any webpage | Overlay appears with Top Center position and Dark theme — settings persisted |

### 14. SPA / Single-Page App Compatibility

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Visit https://gmail.com (or any React/SPA site) | Overlay appears |
| 2 | Navigate between views within the app (e.g. open emails, switch folders) | Overlay remains visible and continues updating |

### 15. Live Preview Reflects Settings

| Step | Action | Expected Result |
|------|--------|-----------------|
| 1 | Open popup | Mini preview viewport shows current stamp at current position |
| 2 | Change Position dropdown to "Top Left" | Preview stamp moves to top-left of mini viewport with animation |
| 3 | Change Theme | Preview stamp background color changes immediately |
| 4 | Change any setting | Live Preview clock continues ticking every second |

---

## Privacy & Security Verification

| Check | Expected Result |
|-------|-----------------|
| Open Chrome DevTools → Network tab on any page | Zero network requests from the extension |
| Check chrome://extensions → DTimestamp Overlay → Permissions | Only "Read and change your data on websites" (required to inject overlay) and "Storage" |
| Open DevTools → Application → Storage | No cookies, localStorage, or sessionStorage written by the extension |
| Review source files | No remote scripts, no eval(), no innerHTML usage anywhere |

---

## No Login Required

This extension has **no authentication, no accounts, no subscription gates, and no
paywalls**. Every feature listed above is available to all users immediately upon
installation with no sign-in of any kind.

The "Buy me a token / coffee" banner in the settings panel links to
https://buymeacoffee.com/hjobanpu — this is a voluntary tip link only and has
absolutely no effect on extension functionality.

---

## Test Credentials

**None required.** No login, no account, no API key, no setup.

---

## Support & Source

- **Homepage:** https://github.com/hjobanpu/DTimestamp-Overlay/
- **Author:** Harihar Jobanputra
