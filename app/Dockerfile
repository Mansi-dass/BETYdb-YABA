FROM python:3.7-slim-buster

COPY . /code

WORKDIR /code

RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    && rm -rf /var/lib/ap?t/lists/*

RUN python -m pip install --upgrade pip \
    && pip install git+https://github.com/aleju/imgaug --no-deps --no-cache-dir \
    && pip install -r requirements.txt --no-cache-dir 


CMD ["python","server.py"]
