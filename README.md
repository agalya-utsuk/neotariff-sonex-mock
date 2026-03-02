# NeoTariff Sonex Mock Service

A lightweight FastAPI mock backend for Sonex integration testing. All endpoints return hardcoded success responses.

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `GET` | `/htsdata/rates/entries` | HTS rates entries |
| `POST` | `/htsdata/context/hts/batch` | HTS context batch |
| `GET` | `/health` | Health check |

All endpoints return:
```json
{}
```

## Setup

### 1. Create and activate a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate       # macOS/Linux
.venv\Scripts\activate          # Windows
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure environment

```bash
cp .env.sample .env
# Edit .env as needed
```

### 4. Run the service

```bash
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

The service will be available at `http://localhost:8000`.

Interactive API docs: `http://localhost:8000/docs`

## Environment Variables

| Variable | Default | Description |
|----------|---------|-------------|
| `HOST` | `0.0.0.0` | Bind address |
| `PORT` | `8000` | Port number |
| `ALLOWED_ORIGINS` | `*` | CORS allowed origins (comma-separated) |
