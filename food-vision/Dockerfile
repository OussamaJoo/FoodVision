FROM python:3.7

## App engine stuff
# Expose the port your app will be running on
EXPOSE 8092

# Upgrade pip
RUN pip install --upgrade pip

# Copy requirements file and install dependencies
COPY requirements.txt /app/requirements.txt
RUN pip install -r /app/requirements.txt

# Copy the application code into the container
COPY . /app

# Set the working directory
WORKDIR /app

# Define the command to run your application
ENTRYPOINT ["streamlit", "run", "app.py", "--server.port=8092", "--server.address=0.0.0.0"]