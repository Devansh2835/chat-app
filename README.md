AI Assistant (Gemini) Setup

1) Install dependencies:

   npm install

2) Set your Gemini API key in environment variable `GEMINI_API_KEY` before starting the server.

   # Windows (PowerShell)
   $env:GEMINI_API_KEY = "your_key_here"
   node app.js

3) Pages:
   - /ai : AI chat interface (requires login)

Notes:
- The server uses the global `fetch` API available in Node 18+ (you mentioned you're on Node 22, so this is supported).
- The AI history is stored in MongoDB in the `aichats` collection and keeps up to 20 items; the UI displays the last 5.
- Gemini API response formats vary; the server attempts common response shapes. If you see "AI service error", check the logs and verify the API key and model endpoint.
