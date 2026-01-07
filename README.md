# Remote Spy Events (Local)

**Remote Spy Events (Local)** is a responsive, client-side Roblox debugging and inspection tool designed for **real-time event monitoring, QA testing, and gameplay analysis**.
It provides a centralized in-game dashboard to observe player interactions, UI behavior, instance changes, and system events without modifying server code.

This tool is intended for **development, QA, and internal testing workflows**.

---

## Key Capabilities

### Real-Time Event Monitoring

Continuously captures and displays gameplay-related events as they occur on the local client.

Supported event categories:

* **INPUT** – Keyboard and mouse input begin/end events
* **SPAWN** – Tracks relevant instances added to the workspace
* **PROMPT** – ProximityPrompt trigger events by the local player
* **SOUND** – Sound playback state changes and SoundId tracking
* **ANIM** – Animation playback events via Animator
* **INSPECT** – Property changes from a selected instance
* **REMOTE / PATH / UI TEXT / GATE / CHEST** – Optional contextual filters

All events are displayed instantly with no polling delay.

---

### Newest-First Log Ordering

Log entries are rendered in reverse chronological order, ensuring:

* The most recent event is always visible at the top
* No need to scroll during rapid event spam
* Better visibility during live debugging sessions

---

### Search and Text Filtering

A live search field allows filtering logs by:

* Event category
* Message content
* Instance path
* Instance class name

Useful for isolating specific prompts, sounds, animation IDs, object paths, or keywords.

---

### Category Toggle System

Each log category includes an ON/OFF toggle to control visibility in real time.

Features:

* Horizontal scrolling toggle bar
* Clean layout on small screens
* Instant re-filtering without clearing logs

---

### ALT + Click Instance Inspector

ALT + Click any object in the world to start monitoring it.

The inspector automatically watches and logs property changes depending on instance type:

**BasePart**

* Position
* CFrame
* Anchored
* CanCollide

**ProximityPrompt**

* Enabled
* ActionText
* ObjectText

**Sound**

* Playing
* SoundId

**Humanoid**

* WalkSpeed
* JumpPower
* Health

**UI Elements (TextLabel / TextButton / TextBox)**

* Text
* Visible

**General**

* Name
* Parent

All detected changes are logged in real time.

---

### Per-Log Copy Button

Each log entry includes a dedicated **COPY** button:

* Copies the log message text to clipboard
* Uses `setclipboard` when available
* Reports status if clipboard access is unavailable

Designed for quick sharing, reporting, or documentation.

---

### Export System (JSON + TXT)

Logs can be exported at any time.

Export includes:

* JSON file (structured data with metadata)
* TXT file (human-readable, newest-first)

Export metadata:

* Place ID
* User ID
* Local timestamp
* Active filters
* Search query
* Selected instance path
* Log count

If file writing is unavailable, export gracefully falls back to clipboard copy.

---

### Session Controls

* **PAUSE** – Temporarily stops logging without clearing data
* **CLEAR** – Resets the current log session instantly

---

### Responsive and Device-Safe UI

The interface automatically adapts to:

* Desktop
* Laptop
* Tablet
* Mobile

Key UI behaviors:

* Always centered on screen
* Scales based on viewport resolution
* Minimum and maximum size clamping
* Clean layout in both landscape and portrait orientations

---

### Usability Features

* Draggable header (mouse devices)
* Minimize button
* Close button
* Smooth button animations
* Consistent typography and spacing

---

## Intended Use

This tool is designed for:

* QA testing
* Gameplay debugging
* UI verification
* Event auditing
* Developer inspection workflows

It operates **entirely on the local client** and does not alter server logic.

---

## Summary

**Remote Spy Events (Local)** provides a structured, real-time view into what is happening on the client during gameplay.
It consolidates event tracking, inspection, filtering, copying, and exporting into a single responsive in-game interface suitable for serious development and QA environments.
