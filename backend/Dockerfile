# Base image
FROM python:3.11-slim

# Set work directory
WORKDIR /app

# Copy requirements first (cache jaoks)
COPY requirements.txt /app/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy kogu backend projekt
COPY . /app/

# Expose port
EXPOSE 8000

# Run server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
