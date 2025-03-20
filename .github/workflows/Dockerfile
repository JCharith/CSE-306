# Use Python 3.9 Alpine as the base image
FROM python:3.9-alpine

# Set the working directory in the container
WORKDIR /app

# Install dependencies (Alpine requires extra packages for pip)
RUN apk add --no-cache gcc musl-dev python3-dev libffi-dev openssl-dev

# Copy the requirements file
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the app
COPY . .

# Command to run the application
CMD ["python", "app.py"]
