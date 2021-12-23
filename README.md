
# aws-cicd

The goal of this project is to demonstrate how to set up a multiple container system using AWS cloudformation.

The containers:

1. A Python program using [`requests`](https://docs.python-requests.org/en/master/) to collect data.
2. The [redis](https://redis.io/) database to store data
3. A [Flask](https://flask.palletsprojects.com/en/2.0.x/) server launched via [gunicorn](https://gunicorn.org/) to server up the data.
4. [Nginx](https://nginx.org/en/) to act as a reverse proxy.

The data used in this example is the current number of confirmed COVID-19 cases from the [COVID-19 API](https://covid19-api.com/).  

The "application" modeled is intentionally minimal: Every 15 minutes, the collector obtains the current count and stores it in the redis database.  The Flask server has a single end point that allows a user to fetch this data.


