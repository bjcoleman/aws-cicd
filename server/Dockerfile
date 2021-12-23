FROM python:3.8.10-slim-buster

WORKDIR /app

COPY server.py .
COPY prod.env .env
COPY requirements.txt .

RUN pip3 install -r requirements.txt

CMD ["gunicorn", "--bind", "0.0.0.0:5000", "server:app"]