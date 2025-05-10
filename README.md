# 🌍 GISelle: A Safer, Smarter Mapping System

**GISelle** is an interactive, safety-focused navigation platform developed as part of the University of Toronto's **ECE297: Communication & Design of Engineering Algorithms** course.  
It combines advanced Geographic Information System (**GIS**) algorithms with real-time responsiveness and a mission-driven UI — designed to make urban travel smarter and safer, especially for **women and vulnerable communities**.

> 💡 **Final Grade:** Awarded an **A** for exceptional algorithmic performance, innovation, and usability testing across all milestones.



## 🎥 Final Demo + UI Showcase
> 📽 Click the image below to watch the full demo on Google Drive 
[![Watch the Full Demo](https://github.com/user-attachments/assets/59628157-f7ff-4ff8-a41a-98264aa2bbea)](https://drive.google.com/file/d/1ZqqvSZlfG-oxGxM2vKJ8t9Unu_PgmEsV/view?usp=sharing)

 

---

## Why GISelle?

Traditional mapping apps often optimize for speed — but not safety. GISelle was built to change that.  
Our system layers intelligent pathfinding with real-world constraints like lighting, emergency rerouting, and shift-specific interfaces to reflect how people *actually* move through cities.

---

This project evolved through several major milestones, each adding new layers of intelligence, usability, and empathy to the platform.  
What follows is a breakdown of each milestone’s goals, algorithms, and feature upgrades — alongside visuals and live demos.

---


## 📌 Milestone 1: Data Integration & Basic Rendering

**Goal:**  
Initialize the GIS system by parsing OpenStreetMap data into a searchable format and rendering it via a basic GUI.

**Core Focus:**
- Parsed `.bin` map data to extract streets, intersections, and POIs.

---


## 🧭 Milestone 2: Intelligent Search & Icon Filtering

**Goal:**  
Empower users to instantly search for street names and identify points of interest — even with limited or partial information — while introducing safety-enhancing visuals.

---


### 🌗 UI Before & After: Day, Night, and Shift Modes

**🕒 Before GISelle Enhancements (Basic UI):**  
Low contrast, minimal feedback, and no safety-specific filters.

| Old UI Preview |
|----------------|
| ![Old UI](https://github.com/user-attachments/assets/7e984fdc-c729-43e6-a729-adcfefb2d603) |

---
#### 🧊 No Shift Applied – Normal Map After Rendering  
The clean, default GISelle interface after core Milestone 2 features were implemented — including search, drawing functions, and initial icon placements.  
This version includes streets, intersections, and POIs rendered via EZGL, but without night or shift-specific styling.

![Raw Map](https://github.com/user-attachments/assets/b0281ca4-620a-4d75-a548-657350177283)


---

#### 🌆 After (Night Shift Mode)  
Highlighting essential services for late-night users like paramedics, students, or women traveling alone.  
This mode emphasizes police stations, hospitals, and transit hubs with high-contrast icons and a darker color palette for visual comfort and rapid decision-making in low-light conditions.

![Screenshot (663)](https://github.com/user-attachments/assets/48414b11-9707-4e36-aaac-da56bbc60577)


---

#### 🌙 After (Dark Mode)  
Designed for users navigating in the evening or indoors.  
Dark Mode reduces glare while preserving all default functionalities — including search, icons, and map interaction — in a visually accessible format.

![Dark Mode UI](https://github.com/user-attachments/assets/0f6687e5-fde6-469c-bf66-03c62842bade)


### 🎯 Icon Filtering System

**Why it matters:**  
In safety-critical environments, clarity and speed matter. Our system allows users to locate police stations, hospitals, and transit hubs with easily scannable icons.

**Features:**
- Icons designed with **distinct night/day modes**.
- Shift-aware coloring for **night-shift workers**.
- Designed for visual accessibility with minimal cognitive load.

📽 [**Watch Demo**](https://drive.google.com/file/d/1yCigekm_2TaZjuh5b4TJdqsYTWXpQuca/view?usp=sharing)

---

#### 🌙 After (Night Mode + Icon Filters)  
Night Mode introduces a dark-themed interface optimized for low-light environments, helping reduce eye strain while maintaining all map functionalities.  
Tailored safety icons make it easier to identify critical locations — even at a glance.

🛡️ **Police Stations, Hospitals, and Transit Points** are highlighted with high-contrast icons and hover tooltips for fast navigation.

**Full UI Preview:**  
![Night UI](https://github.com/user-attachments/assets/61dd6bf4-6028-4be0-8d2e-15b2680e4928)

**Icon Filter Preview (Active):**  
![Icons](https://github.com/user-attachments/assets/1fd3456f-6e00-4236-95f3-7d07f70f8177)



### 🔍 Smart Autocomplete System

**Core Highlights:**
- Developed a custom **Trie** data structure to handle real-time prefix-based search.
- Supported both **full and partial street name matches**, improving UX for urgent or unclear queries.
- Connected search results to **interactive map highlights**, guiding users visually.

📸 **Autocomplete in Action:**
![AutoComplete Result](https://github.com/user-attachments/assets/06da75a2-27ab-4a32-83ea-b96a4fb211db)

---


> _This milestone focused on building trust through intelligent, fast, and safe search — powered by algorithms, but designed for people._


## 🧠 Milestone 3: Smart Pathfinding with A* Algorithm

**Goal:**  
Design a responsive, real-world routing system that considers time, safety, and usability — built around the classic **A\*** search algorithm.

---

### 🚦 Real-World Routing with A*

To move beyond just "shortest distance," our implementation of A\* prioritized:

- ⏱️ **Time-Based Cost Function**  
  Prioritized realistic arrival times over physical distance.

- 🔁 **Turn Penalties**  
  Added time penalties at intersections to simulate real-world travel friction (e.g., waiting at red lights or complex junctions).

- 🛣️ **Main Road Bias**  
  Weighted larger, well-lit roads more heavily for safety and visibility — especially at night.

> 📌 **Technical Insight:**  
> We used a priority queue that balances `g(n)` (actual cost from start) and `h(n)` (heuristic estimate to goal).  
> This drastically reduced the number of nodes explored, maintaining both speed and optimality.

---

### 🧭 Use Case: Finding the Shortest Safe Route

**Scenario 1:**  
User selects two intersections and requests the optimal route.  
The system computes and displays the most efficient, **safest** path — factoring in road types, turn penalties, and time.

📍 **Shortest Path Between 2 Intersections:**  
![Shortest Path](https://github.com/user-attachments/assets/b1b35238-5ac3-4bed-8b18-c45324f1cd41)

---

### 🚓 Use Case: Emergency Re-Routing to Police

**Scenario 2:**  
After selecting a route, the user clicks the **“Find Nearest Police Station”** button.  
GISelle then reroutes to the closest available police station, ideal for emergency situations.

📍 **Shortest Path + Nearest Police Station Redirect:**  
![Police Station Reroute](https://github.com/user-attachments/assets/ca1bc35e-8639-424c-a373-64ed178a19c5)

---

> _Milestone 3 proved that routing is more than math — it’s a reflection of how humans move, make decisions, and seek safety._


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
Extend GISelle’s core functionality to directly support **real-time responsiveness** and **women’s safety** — especially in unfamiliar or high-risk areas.

---

### 🛡️ Key Features

- **Find-Nearest-Police Button**  
  Allows users to instantly reroute to the closest police station in an emergency.  
  📽 [**Watch Demo**](https://drive.google.com/file/d/1yCigekm_2TaZjuh5b4TJdqsYTWXpQuca/view?usp=sharing)

- **Helpline Toggle by Region**  
  Dynamically displays regional helplines, offering support hotlines tailored to the user’s location.  
  📽 [**Watch Demo**](https://drive.google.com/file/d/1mFsIyXOgQFTtLae3_aC17UQoMqpNy3fi/view?usp=sharing)

- **User Testing & Feedback**  
  Conducted **System Usability Scale (SUS)** surveys and timed user trials to validate speed, clarity, and reliability of safety features.

---

### 🌱 Future Additions

- 💡 **Street-Light-Aware Routing**  
  Integrate street-light data for safer nighttime route planning.

- 🚘 **Uber API Integration (Women Rider Preference)**  
  Enable ride-hailing directly from map UI, respecting safety preferences.

- 📍 **Crowdsourced Safety Flagging**  
  Let users tag unsafe areas or report incidents, backed by backend moderation.

---

> _Safety shouldn’t be an afterthought — GISelle puts it at the center of every map interaction._


## 📊 Testing + Results

- **Usability:**  
  System Usability Scale (SUS) scores from 10 participants showed high confidence and ease-of-use.

- **Responsiveness:**  
  Most users found safety buttons in under **2 seconds**.

- **Courier Optimization:**  
  Route time improved by **10–15 seconds** using multi-start and custom 2-opt.

---


## 🧠 Key Learnings

- Algorithm design *directly impacts user safety* when paired with thoughtful UI.
- **Precomputation + Parallelism** = blazing fast responsiveness.
- Metaheuristics like **multi-start and 2-opt** outperform greedy algorithms under real-time constraints.

---

## 👩‍💻 Meet the Team Behind GISelle

Every map, route, and safety feature in GISelle was brought to life by a passionate, all-engineering team dedicated to innovation and impact.  
From algorithms to UI design, we collaborated across disciplines to build a system that reflects both technical depth and real-world empathy.

![Team Photo](https://github.com/user-attachments/assets/1a87ed0e-7e69-4092-959c-0e9b3d8d6b8d)

> _Built with purpose. Designed for safety. Powered by teamwork._


> _Made with care by engineers passionate about safety and smart cities._
