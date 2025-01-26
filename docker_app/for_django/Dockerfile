# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Copy the requirements file into the container at /app
COPY requirements.txt /app/

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the current directory contents into the container at /app
COPY . /app/

# Set environment variables
# This is optional but useful to control Django settings for production
ENV DJANGO_SETTINGS_MODULE=myproject.settings.production
ENV PYTHONUNBUFFERED 1

# Expose the port the app runs on (default Django port is 8000)
EXPOSE 8000

# Run the command to start the Django development server (use gunicorn in production)
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
