# VK-mini-chatapp (rtchatapp)

This repository contains a merged real-time chat application:

- `Chatapp/` — Node.js + Express + Socket.io backend (serves the frontend in production)
- `real-time-chat-app-react/` — React frontend (Vite). Built files are placed in `dist/` and served by the backend.

## Run locally

1. Install dependencies for the backend and frontend (if needed):
```
cd "C:\Users\VENKATA KARTHICK\3D Objects\Message App\Chatapp"
npm install
cd "..\real-time-chat-app-react"
npm install
```

2. Build the frontend production bundle (the backend serves the built app):
```
cd "real-time-chat-app-react"
npm run build
```

3. Start the merged server (serves frontend + socket.io):
```
cd "Chatapp"
npm start
# Open http://localhost:5001
```

## Development (frontend)
During development, you can run the React dev server separately:
```
cd real-time-chat-app-react
npm run dev
# frontend dev server runs on 5173 (or next free port)
```

Note: When developing with the Vite dev server, the frontend connects to the backend socket.io on `http://localhost:5001`.

## Deployment
You can deploy the Node backend (Chatapp) to any Node-compatible host (Render, Railway, Heroku, etc.). Build the frontend on the server or locally and ensure `real-time-chat-app-react/dist` is present before starting the server.

## Structure
- `Chatapp/index.js` — server + socket.io code
- `real-time-chat-app-react/src` — React source

If you want, I can also add a `Procfile` for Heroku or provide deployment steps for Render/Railway.
# rtchatapp