# AI Support Chatbot

- Description: The application allows users to chat with a support agent, persists conversations, and restores chat history on reload using a session-based approach.
<h3> <a href= "https://beautiful-hummingbird-6da801.netlify.app/" >Live Demo</a> </h3>

## How to setup and run the project locally

### Frontend

- Clone the project from GitHub
- Add .env file to the root directory of the frontend project.
- env file details (please do not edit just copy and paste this into the .env file):

  - VITE_API_DEV_URL = http://localhost:4000/api

- Install node packages: `npm i`
- Run the project: `npm run dev`

### Backend

- Clone the project from GitHub
- Add .env file to the root directory of the backend project.
- env file details(please do not edit just copy and paste this into the .env file):

  - PORT = 4000

- Install node packages: `npm i`
- Run the project: `npm run dev`

---

## AI / LLM notes:

- **Groq API**
- Model: `llama-3.1-8b-instant`
  Groq was chosen because it provides a **free**, fast, and production-grade LLM.

#### How I prompting LLM.

- Uses a system prompt to define the AI as a helpful customer support agent.
- Includes domain knowledge such as product categories, shipping policy, return/refund policy, and support hours.
- Sends recent conversation history to provide contextual responses.
- Applies guardrails to prevent hallucinations and out-of-scope answers.
- Limits tokens and message history to control cost and ensure concise replies.

---

## Tech stack

### Frontend

- React
- Vite
- TypeScript

### Backend

- Node.js
- Express
- TypeScript
- PostgreSQL (Supabase)

---

## Features

- AI-powered customer support chat
- Session-based conversations (reload-safe)
- Persistent chat history using PostgreSQL (Supabase)
- Graceful handling of invalid input and AI/API failures
- Clean separation of frontend and backend
- Free LLM integration using **Groq (LLaMA 3.1)**
