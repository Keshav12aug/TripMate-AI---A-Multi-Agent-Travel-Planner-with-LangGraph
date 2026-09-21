✈️ TripMate AI — Multi-Agent Travel Planner with LangGraph

TripMate AI is an intelligent multi-agent travel planning system that transforms natural language travel requests into complete travel plans, including flight recommendations, hotel suggestions, and personalized itineraries.

Built using LangGraph, LangChain, FastAPI, and Groq LLMs, the application demonstrates how multiple specialized AI agents can collaborate to solve a real-world problem through coordinated decision-making and workflow orchestration.

🚀 Project Overview

Planning a trip often requires switching between multiple websites, comparing options, and manually organizing information. TripMate AI streamlines this process by combining specialized AI agents into a single workflow that researches, analyzes, and generates a complete travel plan.

The system includes:

✈️ Flight Research Agent
🏨 Hotel Discovery Agent
🗺️ Itinerary Planning Agent
🤖 Response Generation Agent

All agents work together through a LangGraph-powered orchestration layer to provide a seamless travel planning experience.

✨ Key Features
✈️ Flight Recommendations

Retrieve flight information using the AviationStack API.

🏨 Hotel Research

Discover accommodation options using Tavily-powered web search.

🧠 Multi-Agent Architecture

Leverages multiple specialized agents coordinated through LangGraph workflows.

📝 AI-Generated Travel Itineraries

Creates personalized day-by-day travel plans based on user preferences and constraints.

💾 Persistent Conversation Memory

Stores travel sessions and conversation state using PostgreSQL.

⚡ LLM-Powered Intelligence

Utilizes Groq-hosted language models for fast and accurate reasoning.

🌐 Interactive Web Interface

Simple and responsive frontend built with HTML, CSS, and JavaScript.

🏗️ System Architecture
User Request
      │
      ▼
Travel Planning Workflow (LangGraph)
      │
 ┌────┼────┬─────────┐
 │    │    │         │
 ▼    ▼    ▼         ▼
Flight Hotel Itinerary Final
Agent  Agent Agent   Agent
      │
      ▼
 Consolidated Travel Plan
      │
      ▼
     User
🛠️ Technology Stack
Category	Technologies
Programming	Python 3.10+
Backend	FastAPI
AI Framework	LangGraph, LangChain
LLM	Groq
Database	PostgreSQL
Search	Tavily API
Flight Data	AviationStack API
Frontend	HTML, CSS, JavaScript
Templating	Jinja2
📂 Project Structure
TripMate-AI/
│
├── app.py                  # FastAPI application entry point
├── backend.py              # LangGraph multi-agent workflow
├── requirements.txt        # Project dependencies
│
├── static/                 # Frontend assets
│   ├── style.css
│   └── script.js
│
├── templates/              # HTML templates
│   └── index.html
│
└── tools/                  # External integrations
    ├── flight_tool.py
    └── tavily_tool.py
⚙️ Prerequisites

Before running the application, ensure you have:

Python 3.10 or later
PostgreSQL database
Groq API Key
Tavily API Key
AviationStack API Key
🔑 Environment Variables

Create a .env file in the project root:

DATABASE_URL=postgresql://user:password@localhost:5432/travel_db

GROQ_API_KEY=your_groq_api_key

AVIATIONSTACK_API_KEY=your_aviationstack_api_key

TAVILY_API_KEY=your_tavily_api_key

DEFAULT_ORIGIN_IATA=DAC
📦 Installation
Clone the Repository
git clone https://github.com/yourusername/TripMate-AI.git
cd TripMate-AI
Create Virtual Environment
python -m venv .venv
Activate Environment

Windows

.venv\Scripts\activate

Linux / macOS

source .venv/bin/activate
Install Dependencies
pip install -r requirements.txt
▶️ Running the Application

Start the FastAPI server:

python app.py

Open your browser and visit:

http://127.0.0.1:8000
🔌 API Endpoints
Health Check
GET /health
Travel Planning Endpoint
POST /api/travel
Sample Request
curl -X POST http://127.0.0.1:8000/api/travel \
-H "Content-Type: application/json" \
-d '{
  "message":"Plan a 3-day trip to Tokyo with a budget of $1200"
}'
🔄 Workflow Execution
User submits a travel request.
Flight Agent gathers flight-related insights.
Hotel Agent searches for accommodation options.
Itinerary Agent creates a structured travel schedule.
Final Response Agent consolidates all outputs.
The completed travel plan is returned to the user.
🎯 Learning Outcomes

This project demonstrates:

Multi-Agent AI Systems
LangGraph Workflow Orchestration
Agent-to-Agent Collaboration
LLM Application Development
API Integration
State Management
FastAPI Backend Development
PostgreSQL Integration
Production-Ready AI Architecture
🤝 Contributing

Contributions are welcome!

If you'd like to improve the project:

Fork the repository
Create a feature branch
Implement your changes
Commit and push
Open a Pull Request
🙏 Acknowledgments

This project was created as a practical demonstration of building real-world AI applications using modern agentic frameworks such as LangGraph, LangChain, and FastAPI, combined with travel intelligence APIs and Large Language Models.
