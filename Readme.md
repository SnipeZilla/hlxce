# HLstatsX:CE 1.6.19 (2025)

**A modern, resilient fork of HLstatsX:CE 1.6.19(real-time stats and ranking) designed for srcds multiplayer games, including CS2.**

This fork revives HLstatsX with full support for Source 2 and most importantly community server, asynchronous RCON operations, hybrid log ingestion (UDP & HTTP), and robust, scalable architecture. It's built to perform reliably on both legacy Source servers and the latest CS2 environments — with a strong focus on performance, flexibility, and modern tooling.

---

## 🚀 Features

### ⚡ Async RCON Engine
- Fully non-blocking threaded execution
- Serialized command queuing with built-in timeouts and retry logic
- Runs RCON logic outside the event loop to avoid server lag or script stalls

### 🌐 Dual-Mode Log Ingestion (UDP + HTTP)
- Unified listener handles both legacy srcds (UDP) and CS2’s HTTP-based logging on the **same port**
- Mojo::IOLoop-powered event-driven listener stack
- Built-in detection and normalization of incoming log data

### 🧠 Smart Packet Parsing
- Modular parser system extracts structured data from hybrid log formats
- Dynamic per-server context tracking (map, player stats, hostname, difficulty, etc.)
- Accurate event dispatching across engine types (Source/Source2)

### 🔌 Plugin Support
- **Source 1**: Legacy sourcemod hlstatsx.smx plugin fully supported  
- **Source 2 / CS2**: HLstatsZ plugin for CounterStrikeSharp, emulating the same interface/events used in Sourcemod (Server Mod set as 'SOURCEMOD', Events unchanged hlx_sm_xx)

### 🛠️ Server-Specific Configuration
- Per-server overrides for:
  - Custom commands
  - Stat weighting/modifiers

### 📈 Web Frontend
- Compatible with both:
  - Legacy HLstatsX PHP frontend
  - 🌠 HLstatsZ Next-Gen frontend (fast, AJAX-first):
    - Profile first!
    - DataTables for sorting/filtering
    - OpenStreetMap for geo views
    - ApexCharts for sleek live graphs
    - Built-in caching and query optimization
    - All queries rewrote and optimized for large database
    - ⚠️ Admin pages are not written yet! use ~legacy HLstatsX to setup games.
    

## 💡 Why Choose HLstatsX:CE?
- **HLstatsX is the best and most proven real-time ranking system**, and it's finally been brought into the CS2 era — fully async, extensible, and community-first.
- Keep your players engaged with live stats, leaderboards, and playtime tracking
- Showcase your server community with public profiles and achievements
- Works with *zero client-side changes* — no need to install anything in-game
- Can run on external server: no lag or extra load for your game server
- Battle-tested on thousands of servers across decades of multiplayer gaming

---
