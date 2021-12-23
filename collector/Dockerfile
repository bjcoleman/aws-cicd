FROM python:3.8.10-slim-buster

WORKDIR /app

COPY collector.py .
COPY prod.env .env
COPY requirements.txt .

RUN pip3 install -r requirements.txt

CMD python3 collector.py