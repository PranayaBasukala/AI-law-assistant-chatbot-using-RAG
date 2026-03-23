# Wakalat Sewa - Backend API

FastAPI backend for semantic legal case search.

## Setup

1. **Activate conda environment:**
   ```bash
   conda activate legenv
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the server:**
   ```bash
   python main.py
   ```

   Or with uvicorn directly:
   ```bash
   uvicorn main:app --reload --host 0.0.0.0 --port 8000
   ```

## API Endpoints

- `GET /` - Health check
- `GET /health` - Detailed health status
- `POST /search` - Search legal cases
- `GET /stats` - Database statistics

## API Documentation

Once running, visit:
- Swagger UI: http://localhost:8000/docs
- ReDoc: http://localhost:8000/redoc

## Example Search Request

```bash
curl -X POST "http://localhost:8000/search" \
  -H "Content-Type: application/json" \
  -d '{"query": "murder case", "limit": 5}'
```

