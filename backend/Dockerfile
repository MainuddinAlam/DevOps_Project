# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY ./ /app

# Install any needed packages specified in requirements.txt
RUN pip install -r requirements.txt

# Using port 4000 to expost to the world outside this container
EXPOSE 4000

# Defining environment variable

# Use Gunicorn to run the Flask app
CMD ["gunicorn", "--bind", "0.0.0.0:4000", "app:app"]

# End of File
