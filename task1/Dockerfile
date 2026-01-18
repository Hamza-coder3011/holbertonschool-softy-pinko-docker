FROM ubuntu:latest

# Update and upgrade system
RUN apt-get update
RUN apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix externally managed environment issue (Ubuntu 23+)
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3 (NOT apt)
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy Flask app
COPY ./api.py /app/api.py

# Run the Flask app
CMD ["python3", "/app/api.py"]
