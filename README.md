# 🌍 GISelle: A Safer, Smarter Mapping System

**GISelle** is an interactive, safety-focused navigation system built using advanced Geographic Information System (GIS) algorithms. Designed by a team of engineering students, GISelle enhances traditional street-mapping applications with features tailored toward **women’s safety** and **rapid response**.

This project was developed across multiple milestones as part of a university-level GIS course. Below is a high-level overview of each milestone, its goals, key algorithms, and system enhancements.

---

## 📌 Milestone 1: Data Integration & Basic Rendering

**Goal:**  
Initialize the GIS system by parsing OpenStreetMap data into a searchable format and rendering it via a basic GUI.

**Core Focus:**
- Parsed `.bin` map data to extract streets, intersections, and POIs.

---

## 🧭 Milestone 2: Autocomplete & Search

**Goal:**  
Enable users to search for partial street names and retrieve valid results in real time.

**Core Focus:**
- Built a custom **Trie** data structure for prefix-based search.
- Integrated full-street and partial match functionality.
- Designed an interactive UI using the EZGL graphics library.
- Displayed real-time matching results on the GUI.

**Suggested Media:**
- 📷 *Autocomplete in Action* – Screenshot
- 🎥 *Autocomplete Demo* – [Video Placeholder]

---

## 🧠 Milestone 3: Pathfinding with A* Algorithm

**Goal:**  
Develop a fast and responsive routing system using **A\*** search to compute the optimal path between intersections.

**Core Focus:**
- Implemented the A* algorithm with a **time-based cost function**.
- Added a **turn penalty** to simulate realistic travel behavior.
- Prioritized **main roads** for safety and visibility.

> 📌 *Tech Note:* A* used a priority queue balancing `g(n)` (travel cost) and `h(n)` (heuristic estimate), significantly reducing search space while ensuring optimal routing.

**Suggested Media:**
- 📷 *Shortest Route Rendered on Map* – Screenshot
- 🎥 *A* Search + Emergency Redirects* – [Video Placeholder]

---

## 📦 Milestone 4: Traveling Courier Problem

**Goal:**  
Solve a multi-pickup, multi-dropoff delivery route problem under depot and time constraints using **metaheuristics**.

**Core Focus:**
- Used **Multi-Destination Dijkstra** to precompute travel times.
- Applied **Multi-Start + 2-Opt Simulated Annealing (SA)** for optimization.
- Enabled **parallelism** using `std::thread` for concurrent heuristic execution under 50s time constraints.

**Suggested Media:**
- 📷 *Before vs After Route Optimization* – Diagram
- 🎥 *Courier Algorithm Demo* – [Video Placeholder]

---

## 🔐 Final Features: Safety-Focused Mapping

**Goal:**  
Extend GISelle’s features to prioritize real-world responsiveness and women’s safety.

**Key Features:**
- 🛡️ **Find-Nearest-Police** Button for emergency rerouting.
- 📞 **Helpline Toggle** by region.
- ✅ **Usability Testing** using SUS + timed safety actions.

**Future Additions:**
- 💡 Street-lighting-aware routing
- 🚘 Uber API integration (Women Rider Preference)
- 📍 Crowdsourced safety flagging with backend support

**Suggested Media:**
- 📷 *Emergency Safety UI Overlay* – Screenshot
- 🎥 *Emergency Feature Demo* – [Video Placeholder]

---

## 📊 Testing + Results

- **Usability:**  
  System Usability Scale (SUS) scores from 10 participants showed high confidence and ease-of-use.

- **Responsiveness:**  
  Most users found safety buttons in under **2 seconds**.

- **Courier Optimization:**  
  Route time improved by **10–15 seconds** using multi-start and custom 2-opt.

---

## 🔮 What’s Next?

GISelle’s mission continues:
- 🌃 Integrate API-driven **street-lighting mode**
- 🚗 Enable **Uber Women Preference** rides directly from map
- 🧭 Launch **community-driven safety reporting**

---

## 🧠 Key Learnings

- Algorithm design *directly impacts user safety* when paired with thoughtful UI.
- **Precomputation + Parallelism** = blazing fast responsiveness.
- Metaheuristics like **multi-start and 2-opt** outperform greedy algorithms under real-time constraints.

---

## 🎥 Want the Full Demo?

- 👉 [Watch Our Final Presentation Demo](#)
- 👉 [Explore Our Poster Slide Deck](#)

---

> _Made with care by engineers passionate about safety and smart cities._
