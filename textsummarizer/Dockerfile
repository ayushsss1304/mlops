# Use a base image with Python
FROM python:3.10-slim

# Set the working directory
WORKDIR /app

# Copy requirement file and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of your code
COPY . .

# Run main.py once during container build or on start (depending on what it does)
# If it's for model setup or download, do it here:
RUN python main.py

# Set default command to run app.py (Flask/FastAPI server)
CMD ["python", "app.py"]
