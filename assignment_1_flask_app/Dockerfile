FROM python:3.11-alpine

WORKDIR /flask-app

# Copy requirements
COPY requirements.txt .

# Install dependencies including gunicorn
RUN pip install -r ./requirements.txt

# Copy app source
COPY . .

# Default command to run the app
CMD ["gunicorn", "--workers", "3", "--bind", "0.0.0.0:8080","app:app"]