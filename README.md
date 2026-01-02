---

# Trade Opportunities API

## 📌 Project Overview

This project implements an **end-to-end API** that analyzes current market data and provides **trade opportunity insights** for specific sectors in India.
The API accepts a sector name and returns a **structured markdown report** containing market trends, opportunities, risks, and insights.

The solution is built as part of a **Python assessment task** and follows clean architecture, security best practices, and in-memory data handling.

---

## 🛠 Tech Stack

* **Python 3**
* **FastAPI** – Backend API framework
* **Google Gemini API** – AI-based market analysis
* **DuckDuckGo Search** – Market data collection
* **Uvicorn** – ASGI server
* **In-memory storage** (no database)

---

## 📂 Project Structure

```
app/
├── api/
│   └── routes.py       # API endpoints
├── core/
│   ├── config.py       # Configuration
│   └── security.py     # Authentication & rate limiting
├── services/
│   ├── ai_analyzer.py  # Gemini AI integration
│   └── market_data.py  # DuckDuckGo data collection
└── main.py             # Application entry point
```

---

## 🚀 How to Run the Project

### 1️⃣ Install dependencies

```bash
pip install fastapi uvicorn requests
```

### 2️⃣ Set environment variable (if required)

```bash
export GEMINI_API_KEY=your_api_key
```

### 3️⃣ Run the API

```bash
uvicorn app.main:app --reload
```

---

## 🔗 API Usage

### Endpoint

```
GET /analyze/{sector}
```

### Allowed Sectors

* pharmaceuticals
* technology
* agriculture

### Example Request

```
GET /analyze/pharmaceuticals
```

### Example Response

The API returns a **structured markdown report**, including:

* Market overview
* Recent trends
* Trade opportunities
* Risks & challenges
* AI-generated insights

The response can be directly saved as a `.md` file.

---

## 🔐 Authentication

* Simple token-based authentication is implemented
* Each request must include a valid token
* Unauthorized requests are rejected

---

## ⏱ Rate Limiting

* Rate limiting is applied **per user/session**
* Prevents abuse and excessive API calls
* Implemented in-memory

---

## 🔍 Data Collection

* **DuckDuckGo search** is used for market data collection
* Relevant news, articles, and market signals are fetched
* Data is passed to the AI analyzer for insight generation

---

## 🧠 AI Analysis

* Google Gemini API is used to analyze collected market data
* Generates structured insights and summaries
* Error handling is implemented for external API failures

---

## ⚠️ Limitations

* Market data depends on publicly available search results
* In-memory storage resets on server restart
* API insights depend on LLM response quality

---

## 🔮 Future Improvements

* Add caching for repeated sector requests
* Support more sectors dynamically
* Improve real-time market data sources
* Add unit tests and monitoring

---

## ✅ Assessment Compliance

* ✔ Python-based solution
* ✔ Public GitHub repository
* ✔ `.ipynb` implementation
* ✔ README documentation
* ✔ No ZIP or Google Drive links
* ✔ Follows security & rate limiting requirements

---

## 👤 Author

Sachin Kallappa Hebbale



Just tell me 👍
