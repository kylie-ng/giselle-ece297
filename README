🌍 GISelle: A Safer, Smarter Mapping System
GISelle is an interactive, safety-focused navigation system built using advanced Geographic Information System (GIS) algorithms. Designed by a team of engineering students, GISelle enhances traditional street-mapping apps with features tailored for women’s safety and emergency responsiveness.

This project was developed through multiple course-based milestones. Each stage introduced new algorithms, UI features, and real-time optimizations.

📌 Milestone 1: Data Integration & Basic Rendering
Goal:
Set up the foundation by parsing OpenStreetMap data and rendering it using a custom interface.

Highlights:

Extracted streets, intersections, and POIs from .bin map data

Built a dynamic UI using the EZGL graphics library

Added intuitive zoom, pan, and hover interaction

Media:
📷 Screenshot: Map Rendering Demo
🎥 Video: EZGL Interface Walkthrough

🧭 Milestone 2: Autocomplete & Search
Goal:
Support partial street name search with real-time results.

Highlights:

Created a Trie structure for prefix-based search

Supported full-street + partial matching

Displayed suggestions live on the GUI

Media:
📷 Screenshot: Autocomplete in Action
🎥 Video: Autocomplete Demo

🧠 Milestone 3: A* Pathfinding
Goal:
Use A* to find the fastest, safest path between intersections.

Highlights:

Implemented A search* with time-based cost

Added turn penalties to simulate realistic travel

Prioritized well-lit/main roads for user safety

⏱️ A balanced g(n) and h(n) via a priority queue to speed up search while ensuring optimal routing.

Media:
📷 Screenshot: Shortest Route Display
🎥 Video: A* Pathfinding + Emergency Redirect

📦 Milestone 4: Traveling Courier Problem
Goal:
Solve multi-pickup, multi-dropoff routing with depot constraints using optimization techniques.

Highlights:

Built a Multi-Destination Dijkstra precomputation layer

Used Multi-Start + 2-Opt Simulated Annealing

Boosted speed with parallel threads using std::thread

⚠️ Note: Traditional SA didn’t help under time pressure — we instead tuned our heuristics for better real-time performance.

Media:
📷 Diagram: Before vs After Route Optimization
🎥 Video: Courier Algorithm in Action

🔐 Final Safety Features
Goal:
Transform GISelle into a true safety-first navigation tool.

Features Added:

🚨 Nearest Police Station button with instant reroute

📞 Emergency Helpline Toggle (region-specific)

🧪 User Testing via SUS and action time tracking

Future Plans:

💡 Routing aware of street lighting

🚘 Integration with Uber Women Preferred Ride

🗺️ Crowdsourced safety flagging backend

Media:
📷 Screenshot: Emergency UI Overlay
🎥 Demo: Safety Feature Showcase

📊 Testing & Results
✅ Usability: 10 participants rated GISelle highly in confidence & clarity (SUS test)

⚡ Responsiveness: 80% located safety buttons in <2 seconds

📦 Efficiency: Route times improved 10–15s with heuristics

🔮 What's Next?
GISelle is evolving to serve more users in safer, smarter ways:

🌃 Streetlight-aware routing

🚗 Seamless Uber integration for safer rides

🧭 Community-led safety reporting

🧠 Key Learnings
Great algorithm design enhances safety when combined with user-centered UI

Precomputation + parallelism = ultra-fast performance

Heuristics like Multi-Start + 2-Opt outperform greedy approaches in real time

🎥 Watch It In Action
👉 Final Presentation Demo
👉 Poster Slide Deck

Made with purpose by a team of engineers passionate about building safe, smart, and inclusive technology.
