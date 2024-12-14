# htpasswd 

## Usage

To generate a password file:


```Docker
FROM python:latest

# Set working directory
WORKDIR /app

# Copy requirements file
COPY requirements.txt .

# Install dependencies
RUN pip install -r requirements.txt
docker run --rm -ti xmartlabs/htpasswd <username> <password> > htpasswd
``Docker
FROM python:latest

## Install Bash
RUN apt-get update && apt-get install -y bash

## Copy requirements file
COPY requirements.txt .

## Install dependencies
RUN pip install -r requirements.txt

## Set working directory
WORKDIR /app

## Copy application code
COPY . .

## Run Bash
CMD ["bash"]

This will use bcrypt encryption.
