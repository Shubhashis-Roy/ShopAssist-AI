# AI Support Chatbot

- Description: The application allows users to chat with a support agent, persists conversations, and restores chat history on reload using a session-based approach.
<h3> <a href= "https://beautiful-hummingbird-6da801.netlify.app/" >Live Demo</a> </h3>

## Features

- AI-powered customer support chat
- Session-based conversations (reload-safe)
- Persistent chat history using PostgreSQL (Supabase)
- Graceful handling of invalid input and AI/API failures
- Clean separation of frontend and backend
- Free LLM integration using **Groq (LLaMA 3.1)**

---

## AI / LLM notes:

- **Groq API**
- Model: `llama-3.1-8b-instant`
  Groq was chosen because it provides a **free**, fast, and production-grade LLM.

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

#### How I prompting LLM.

- Uses a system prompt to define the AI as a helpful customer support agent.
- Includes domain knowledge such as product categories, shipping policy, return/refund policy, and support hours.
- Sends recent conversation history to provide contextual responses.
- Applies guardrails to prevent hallucinations and out-of-scope answers.
- Limits tokens and message history to control cost and ensure concise replies.


