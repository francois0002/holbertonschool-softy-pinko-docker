FROM ubuntu:latest

# Update APT package index
RUN apt-get update

# Upgrade installed packages
RUN apt-get upgrade -y

# Update the package list and install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Manage the error "his environment is externally managed "
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Set /app as the working directory
WORKDIR /app

# Copy the local api.py file to the working directory in the Docker image
COPY ./api.py /app/api.py

# Expose port 5252 to allow external access
EXPOSE 5252

# Command to run the Flask application
CMD ["python3", "api.py"]
