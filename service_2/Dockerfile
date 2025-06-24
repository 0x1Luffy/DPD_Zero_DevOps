FROM python:3.11-alpine
WORKDIR /app

# Install system dependencies
RUN apk add --no-cache curl

# Install uv and Python dependencies system-wide
RUN pip install --no-cache-dir uv
RUN uv pip install --system flask

# Copy application code
COPY app.py .

EXPOSE 8002
CMD ["uv", "run", "app.py"]