# Dockerfile for Task 1
FROM ubuntu:latest

# Update and upgrade the base image
RUN apt-get update && apt-get upgrade -y

# Install Python3, pip, and venv
RUN apt-get install -y python3 python3-pip python3-venv

# Create a virtual environment
RUN python3 -m venv /opt/venv

# Activate the virtual environment and install Flask
RUN /opt/venv/bin/pip install flask

# Set the environment PATH to use the virtual environment
ENV PATH="/opt/venv/bin:$PATH"

# Set the working directory
WORKDIR /app

# Copy the application file into the container
COPY ./api.py /app/api.py

# Default command to run your application
CMD ["python3", "/app/api.py"]

