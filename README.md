# 🎬 ShowBuddy – AI TV Show Recommender & Watchlist Assistant

ShowBuddy is an interactive, AI-powered TV show discovery tool that helps users quickly find what to watch next.  
It provides personalized recommendations, genre-based suggestions, watchlist management, and cleanly formatted AI answers — all inside a smooth web-based interface.

This project is perfect for personal use, demos, portfolio showcases, and as a foundation for a more advanced recommender system.

---

## 🚀 Features

### ⭐ 1. AI-Powered Recommendations  
Get smart, structured TV show suggestions using Google Gemini.  
Each recommendation includes:
- Show Title  
- Short Description  
- IMDb Rating  
- Platform Availability  

### ⭐ 2. Personalized Watchlist  
- Add shows to your watchlist  
- Remove or clear items  
- Persistent storage using `localStorage`  
- Ask for recommendations *based on what you already like*  

### ⭐ 3. One-Click Genre Discovery  
Instant recommendations for:
- Crime  
- Comedy  
- Fantasy  
- Sci-Fi  
- Drama  
- Horror  
- Documentaries  
…and more!

### ⭐ 4. Clean Markdown Formatting  
AI responses are auto-converted into clean HTML:
- Removes `****`  
- Makes lists readable  
- Adds bold/italics  
- Perfect for UI display  

### ⭐ 5. Custom API Key Support  
Enter your Gemini API key in the Settings panel.  
Stored securely in your browser (not uploaded anywhere).

---

## 🏗 Architecture

## 🏗 Architecture Diagram

## 🏗 Architecture Diagram

```mermaid
flowchart TD

A[User Browser<br/>HTML + CSS + JS] --> B[Frontend Logic]

subgraph Frontend Logic
    B1[Chat System]
    B2[Watchlist Manager]
    B3[Genre Buttons]
    B4[Markdown Formatter]
    B5[API Key Settings]
end

B --> C[Google Gemini API]

subgraph Google Gemini API
    C1[Recommendation Engine]
    C2[Similar Shows]
    C3[Genre Suggestions]
end


### 🔎 Component Breakdown

#### **1. UI Layer**
- Renders chat window, genre sidebar, watchlist.
- Handles user interactions.

#### **2. Application Logic (JavaScript)**
- Builds structured prompts for the Gemini model.
- Cleans and formats AI markdown.
- Stores persistent state in browser.

#### **3. Gemini LLM Engine**
- Processes natural language queries.
- Returns structured recommendation texts.


---

## 🛠 Tech Stack

### **Frontend**
- HTML5  
- CSS3  
- JavaScript (ES6)  
- LocalStorage API  
- Fetch API  

### **AI / LLM**
- Google Gemini API  
- Models Supported:  
  - `gemini-2.0-flash`  
  - `gemini-pro`  

## 📁 Project Structure

showbuddy/
│── index.html
│── README.md
│── /config
│ └── .env.example
│── requirements.txt


---

## 🔧 Setup & Run Guide

### ✔ Prerequisites
- Any modern browser  
- A Google Gemini API key (free tier works)  

---

### ✔ 1. Clone the Repository

```bash
git clone https://github.com/Atul-Mor/showbuddy.git
cd showbuddy

### ✔ 2. Run Locally

Option A — Just open the HTML file

Double-click:

index.html

Option B — Recommended: Run using a local server

### Using Python
python3 -m http.server 8000

Then open:

http://localhost:8000

---

🔮 What’s Next? (Planned Enhancements)

Add Flask/FastAPI backend

Add FAISS embeddings for similarity-based recommendations

Add Movies, not just TV series

Add login + cloud watchlist sync

Multi-language support

Platform filtering (e.g., Netflix-only)

UI redesign with Tailwind or React version
