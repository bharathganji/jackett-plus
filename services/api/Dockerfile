# Use official Python 3.12 slim image
FROM python:3.12-slim

WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy application source
COPY . .

# Default environment variables
ENV JACKETT_API_URL=http://127.0.0.1:9117
ENV PORT=9889

EXPOSE 9889

# Production CMD
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "9889"]
