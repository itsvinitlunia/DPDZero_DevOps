FROM python:3.11-slim

WORKDIR /app

# Installing uv
RUN pip install uv

# Copy project files
COPY . .

# Install dependencies using uv
RUN uv pip install -e .

EXPOSE 8082

CMD ["python", "app.py"]