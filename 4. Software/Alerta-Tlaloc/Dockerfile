
FROM python:3.11-slim

WORKDIR /app

# Instalar dependencias
COPY backend/requirements.txt ./requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

# Copiar el backend y los modelos
COPY backend/ ./backend/

# Puerto utilizado por Render
EXPOSE 10000

# Iniciar FastAPI
CMD ["sh", "-c", "uvicorn backend.Server:app --host 0.0.0.0 --port ${PORT:-10000}"]
