# Dockerfile for Office Management System (Django)
FROM python:3.12-slim

ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

WORKDIR /app

# Copy and install deps (expects requirements.txt with at least 'Django')
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy project code (place this Dockerfile inside the Django folder: office_emp_proj/ )
COPY . .

EXPOSE 8000

CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
