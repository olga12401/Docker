# Use an official Python runtime as a parent image
FROM python:3.8-slim

# Set the working directory in the container
WORKDIR /app

# Copy only the requirements.txt first to leverage Docker cache
COPY appfiles/requirements.txt /app/

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r /app/requirements.txt

# Now copy the rest of your application's files into the container
COPY appfiles/ /app/

# Make port 80 available to the world outside this container
EXPOSE 80

# Define environment variable 
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]