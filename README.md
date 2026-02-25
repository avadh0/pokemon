# 🧩 Pokedex Web App

A fully interactive **Pokedex web application** built using **HTML, CSS, and Vanilla JavaScript**, designed to demonstrate strong fundamentals of frontend development, API integration, and dynamic UI rendering.

This project focuses on **clean architecture, performance optimization, and user experience**, making it suitable for showcasing in technical interviews.

---

## 🚀 Live Demo

🔗 **Netlify Deployment:**
👉 [https://your-netlify-link-here.netlify.app](https://celadon-cranachan-1864c.netlify.app/)


---

## 🎯 Project Objective

The goal of this project is to:

* Build a **dynamic frontend application without frameworks**
* Practice **API integration**
* Implement **search, filtering, and navigation**
* Design a **responsive UI system**
* Understand **state management using vanilla JS**

---

## ✨ Features

### 🔍 1. Real-Time Search

* Users can search Pokémon by:

  * **ID (number-based filtering)**
  * **Name (string-based filtering)**
* Implemented using **event-driven input handling**
* Shows **"Pokemon not found"** when no match

---

### 🔃 2. Sorting Mechanism

* Toggle between:

  * Sorting by **number**
  * Sorting by **name**
* Implemented using **radio buttons + filtering logic**

---

### 📄 3. Pokémon Listing Page

* Displays first **151 Pokémon (Gen 1)**
* Each card shows:

  * Pokémon image (SVG)
  * Name
  * ID
* Uses **dynamic DOM creation**

---

### 📊 4. Pokémon Detail Page

Displays complete information of a selected Pokémon:

* Name and ID
* Types (with color coding)
* Height & Weight
* Abilities
* Description (from species API)
* Base stats (visualized with progress bars)

---

### 🎨 5. Dynamic Theming

* Background color changes based on Pokémon type
* Uses a **type-to-color mapping system**
* Applies styles dynamically using JavaScript

---

### 🔁 6. Navigation System

* Next / Previous Pokémon buttons
* URL updates using **History API**
* No full page reload required

---

### ⚡ 7. Performance Optimization

* Uses `Promise.all()` for **parallel API requests**
* Minimizes DOM reflows by batching updates
* Efficient filtering using **local state**

---

## 🛠️ Tech Stack

* **HTML5** – Structure
* **CSS3** – Styling (Flexbox + Variables)
* **JavaScript (ES6+)** – Logic
* **PokeAPI** – Data Source

---

## 🧱 Architecture Overview

This project follows a **modular structure**:

```id="arch1"
UI (HTML + CSS)
      ↓
Event Handling (search.js)
      ↓
Data Fetching (pokemon.js / pokemon-detail.js)
      ↓
Rendering Logic (DOM Manipulation)
```

---

## 📂 Project Structure

```id="struct1"
project-root/
│
├── index.html              # List page
├── detail.html             # Detail page
│
├── style.css               # Global styles & design system
│
├── pokemon.js              # Fetch & render Pokémon list
├── pokemon-detail.js       # Detail page logic
├── search.js               # UI interactions (search & filter)
│
└── assets/                 # Icons and images
```

---

## ⚙️ Core Functionalities Explained

### 🔹 1. Data Fetching Strategy

```id="code1"
Promise.all([
  fetch(pokemon),
  fetch(pokemonSpecies)
])
```

* Fetches **multiple APIs in parallel**
* Reduces loading time
* Improves performance

---

### 🔹 2. State Management (Vanilla JS)

```id="code2"
let allPokemons = [];
let currentPokemonId = null;
```

* Stores fetched data locally
* Avoids repeated API calls
* Controls UI updates

---

### 🔹 3. Dynamic Rendering

* HTML elements are created using JavaScript
* Data is injected into the DOM

```id="code3"
const listItem = document.createElement("div");
listItem.innerHTML = `...`;
```

---

### 🔹 4. Search Algorithm

```id="code4"
pokemon.name.toLowerCase().startsWith(searchTerm)
```

* Case-insensitive search
* Supports number & name filtering

---

### 🔹 5. URL-Based Navigation

```id="code5"
detail.html?id=25
```

* Uses **query parameters**
* Enables direct navigation to any Pokémon

---

### 🔹 6. History API Usage

```id="code6"
window.history.pushState({}, "", `?id=${id}`);
```

* Updates URL without page reload
* Simulates SPA behavior

---

### 🔹 7. Dynamic Styling

```id="code7"
element.style.backgroundColor = color;
```

* UI changes based on Pokémon type
* Improves visual feedback

---

## 🧠 Key Concepts Demonstrated

* DOM Manipulation
* Event Handling
* Async/Await & Fetch API
* Promise.all()
* State Management
* Dynamic UI Rendering
* CSS Variables (Design System)
* Flexbox Layout
* URL Routing (Query Params)

---

## ⚠️ Challenges & Solutions

### 1. API Delay / Race Conditions

* **Problem:** UI could update with old data
* **Solution:** Used `currentPokemonId` to validate responses

---

### 2. Multiple API Calls

* **Problem:** Slower loading
* **Solution:** Used `Promise.all()` for parallel requests

---

### 3. UI State Handling

* **Problem:** Managing search & filters
* **Solution:** Used class-based state toggling

---

### 4. Dynamic Styling

* **Problem:** Different Pokémon types need different UI
* **Solution:** Created a **type-color mapping system**

---

## 🚀 How to Run Locally

```id="run1"
git clone https://github.com/your-username/pokedex.git
cd pokedex
open index.html
```

---

## 📈 Future Improvements

* Add pagination / infinite scroll
* Add favorites (localStorage)
* Add caching for API data
* Convert to React for scalability
* Add animations & transitions
* Improve accessibility



---

## 🧑‍💻 Author

**Ankit Yadav**

* Computer Science Engineering Student
* Interested in Software Development & Web Technologies

---

## ⭐ Why This Project Matters

This project showcases:

* Strong JavaScript fundamentals
* Clean architecture without frameworks
* Ability to work with real APIs
* UI/UX thinking
* Problem-solving skills

---

## 📄 License

This project is open-source and available under the MIT License.

