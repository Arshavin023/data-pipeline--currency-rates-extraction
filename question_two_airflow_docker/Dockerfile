FROM apache/airflow:latest-python3.8

USER root
RUN apt-get update && \
    apt-get -y install git && \
    apt-get clean

USER airflow
# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container at /app
COPY ./requirements.txt /app/requirements.txt
RUN pip install --user --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt