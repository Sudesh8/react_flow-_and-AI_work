# AI React Flow Workflow Project

This project is an automation and security-simulation workflow designed to demonstrate how user input can be processed through a visual decision pipeline using AI.

The application combines a visual workflow (React Flow), a backend API (Flask), and an AI model (Google Gemini) to simulate real-world approval and validation systems.

---

## Why This Project

The purpose of this project is to show:
- How a frontend workflow diagram can represent logical decision paths
- How AI can be integrated into backend automation
- How conditional logic (TRUE / FALSE paths) can trigger different actions
- How frontend, backend, and AI services communicate in a clean architecture

This type of pattern is commonly used in security checks, approval flows, monitoring systems, and automated responses.

---

## High-Level Architecture

1. User interacts with the React Flow UI
2. User enters a message and a keyword
3. Frontend sends data to Flask backend via API
4. Backend sends the data to Google Gemini
5. Gemini evaluates whether the keyword exists in the message
6. Based on the result:
   - TRUE path → generates a structured email and sends it to a webhook
   - FALSE path → returns a denied or suggestion message
7. The result is shown back in the UI

---
<img width="1912" height="950" alt="image" src="https://github.com/user-attachments/assets/85ac9f9f-2361-4b7f-a79d-6e4b976bd080" /> 

## Tech Stack Used

Frontend:
- React.js for UI logic
- React Flow for visual workflow representation

Backend:
- Python with Flask for API handling and orchestration

AI Model:
- Google Gemini 2.5 Flash for fast and lightweight AI reasoning

Simulation:
- Webhook.site to simulate sending email output to an external system

---

## Backend Setup (Python / Flask)

Go to backend folder:
cd backend

Install dependencies:
pip install -r requirements.txt

Create .env file and add:
GOOGLE_API_KEY=your_google_api_key_here

Start backend server:
python backend_api.py

Backend URL:
http://localhost:5000

---

## Frontend Setup (React)

Go to frontend folder:
cd frontend

Install dependencies:
npm install

Start frontend:
npm run dev

Open in browser:
http://localhost:5173

---

## Workflow Logic Explanation

Input:
- User message
- Target keyword

Processing:
- Gemini checks whether the keyword exists in the user message
- The decision is deterministic and controlled for predictable behavior

Output:
- TRUE path:
  - AI generates a formal email format
  - Email content is sent to a webhook endpoint
- FALSE path:
  - AI returns a denial or suggestion response
  - No webhook action is triggered

---

## Why React Flow Was Used

React Flow allows complex logic to be represented visually.
This makes workflows:
- Easier to understand
- Easier to debug
- More intuitive for non-technical users

It also mirrors real automation platforms used in enterprise environments.




