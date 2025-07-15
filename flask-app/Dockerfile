# Using outdated image
FROM ubuntu:20.04

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip3 install --no-cache-dir -r /app/requirements.txt

WORKDIR /app
COPY app.py .
COPY requirements.txt .

CMD ["python3", "app.py"]
