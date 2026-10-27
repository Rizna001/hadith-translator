# JSON Chapter Translator

A React and Express app for translating JSON chapter files while preserving
their structure. AI-powered translations use the Google Gemini API.

## Requirements

- Node.js 22.12.0 or later
- npm
- A Gemini API key for translations

## Run locally

1. Copy `.env.example` to `.env` and set `GEMINI_API_KEY` to your key.
2. Install dependencies with `npm install`.
3. Start the development server with `npm run dev`.
4. Open the local URL printed by the server (usually `http://localhost:3000`).

To check a production build locally, run `npm run build` and then `npm start`.

## Deploy to Render

1. Push this project folder to a GitHub repository.
2. In Render, choose **New +** → **Blueprint** and connect that repository.
   Render will read `render.yaml` to configure the web service.
3. In the Render service's environment settings, set `GEMINI_API_KEY` to a
   valid key. Do not commit the real key or put it in frontend code.
4. Deploy. Render builds the Vite frontend and Express server, then starts the
   server using the port provided by Render.
5. Verify the deployment at `/api/health`. Translation requests require the
   Gemini API key to be configured.

The `.env` file is ignored by Git. `.env.example` is safe to commit and contains
only a placeholder.
