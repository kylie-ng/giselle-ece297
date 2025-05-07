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

**GISelle day VS NightMode and NightShift:**
![icons_GISelle](https://github.com/user-attachments/assets/1fd3456f-6e00-4236-95f3-7d07f70f8177)
![Screenshot (644)](https://github.com/user-attachments/assets/61dd6bf4-6028-4be0-8d2e-15b2680e4928)

# 🎯 Icons Filtering System
[📽 **View Demo**](https://drive.google.com/file/d/1yCigekm_2TaZjuh5b4TJdqsYTWXpQuca/view?usp=sharing)
A clean, responsive, and user-friendly **icon filtering tool** that allows users to easily search, sort, and filter icons by category, tag, or keyword. Perfect for developers, designers, or anyone who needs quick access to the right icon — fast and fuss-free.

**AutoComplete:**
![Screenshot (646)](https://github.com/user-attachments/assets/06da75a2-27ab-4a32-83ea-b96a4fb211db)


---

## 🧠 Milestone 3: Pathfinding with A* Algorithm

**Goal:**  
Develop a fast and responsive routing system using **A\*** search to compute the optimal path between intersections.

**Core Focus:**
- Implemented the A* algorithm with a **time-based cost function**.
- Added a **turn penalty** to simulate realistic travel behavior.
- Prioritized **main roads** for safety and visibility.

> 📌 *Tech Note:* A* used a priority queue balancing `g(n)` (travel cost) and `h(n)` (heuristic estimate), significantly reducing search space while ensuring optimal routing.

**Shortest Path Between 2 Intersections:**
![Screenshot (648)](https://github.com/user-attachments/assets/b1b35238-5ac3-4bed-8b18-c45324f1cd41)

**Shortest Path Between 2 Intersections AND AFTER Clicking find Nearest Police Station:**
![Screenshot (649)](https://github.com/user-attachments/assets/ca1bc35e-8639-424c-a373-64ed178a19c5)


---

## 📦 Milestone 4: Traveling Courier Problem

**Goal:**  
Solve a multi-pickup, multi-dropoff delivery route problem under depot and time constraints using **metaheuristics**.

**Core Focus:**
- Used **Multi-Destination Dijkstra** to precompute travel times.
- Applied **Multi-Start + 2-Opt Simulated Annealing (SA)** for optimization.
- Enabled **parallelism** using `std::thread` for concurrent heuristic execution under 50s time constraints.

---

## 🔐 Final Features: Safety-Focused Mapping

**Goal:**  
Extend GISelle’s features to prioritize real-world responsiveness and women’s safety.

**Key Features:**
- 🛡️ **Find-Nearest-Police** Button for emergency rerouting.
[📽 **View Demo**](https://drive.google.com/file/d/1yCigekm_2TaZjuh5b4TJdqsYTWXpQuca/view?usp=sharing)
- 📞 **Helpline Toggle** by region.
[📽 **View Demo**](https://drive.google.com/file/d/1mFsIyXOgQFTtLae3_aC17UQoMqpNy3fi/view?usp=sharing)
- ✅ **Usability Testing** using SUS + timed safety actions.

**Future Additions:**
- 💡 Street-lighting-aware routing
- 🚘 Uber API integration (Women Rider Preference)
- 📍 Crowdsourced safety flagging with backend support

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

## 🎥 ** My Amazing Team! **
![Screenshot (650)](https://github.com/user-attachments/assets/1a87ed0e-7e69-4092-959c-0e9b3d8d6b8d)



---

> _Made with care by engineers passionate about safety and smart cities._
