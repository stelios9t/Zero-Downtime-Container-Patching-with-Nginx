# Intially used outdated image
# FROM ubuntu:18.04
FROM ubuntu:20.04

WORKDIR /app

COPY requirements.txt .

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    pip3 install --no-cache-dir --upgrade pip setuptools wheel && \
    pip3 install --no-cache-dir -r requirements.txt

COPY app.py .

CMD ["python3", "app.py"]



