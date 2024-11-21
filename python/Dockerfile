ARG PYTHON_VERSION=3.11-alpine
FROM python:${PYTHON_VERSION}

# Update git
RUN apt-get update && \
    apt-get install -y \
    git \
    && apt-get clean \

WORKDIR /app

# Install dependencies
COPY requirements.txt /app/requirements.txt
RUN pip install --upgrade pip
RUN pip install -r requirements.txt

# Copy the rest of the files.
COPY . /app