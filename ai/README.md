# AI Chat Backend API - Railway Deployment

FastAPI backend for AI chat using Ollama. This is the backend-only branch for Railway deployment.

## Setup

### Backend (Railway)

1. Install Ollama locally: https://ollama.com
2. Pull a model: `ollama pull llama2`
3. Start Ollama: `ollama serve`

### Deploy to Railway

1. Connect your GitHub repo to Railway
2. Railway will auto-detect the Python app
3. Set environment variables:
   - `OLLAMA_URL`: Your Ollama server URL (or use ngrok for local)
   - `OLLAMA_MODEL`: Model name (default: "llama2")
   - `PORT`: Railway sets this automatically

### Local Development

```bash
cd backend
pip install -r requirements.txt
python main.py
```

The API will run on http://localhost:8000

## API Endpoints

- `GET /` - Health check
- `POST /api/chat` - Send message, get AI response
  ```json
  {
    "message": "Hello, how are you?"
  }
  ```

