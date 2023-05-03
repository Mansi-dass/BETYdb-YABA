FROM python:3.7-slim-buster
# FROM python:3.7.2-slim
# FROM ubuntu

COPY . /code

WORKDIR /code

RUN apt-get update && apt-get install -y --no-install-recommends \
    git=2.40.1-1 \
    && rm -rf /var/lib/apt/lists/*

RUN /usr/local/bin/python -m pip install --upgrade pip \
    && pip install git+https://github.com/aleju/imgaug --no-deps --no-cache-dir \
    && pip install -r requirements.txt --no-cache-dir

    #  \
    # python3 \
    # python-pip

# RUN apt-get update && apt-get install -y \
#     python3-pip \
#     git 
# && rm -rf /var/lib/apt/lists/*


# RUN pip install --upgrade pip \
#     && pip install git+https://github.com/aleju/imgaug --no-deps \
#     && pip install -r requirements.txt    

# RUN pip install --upgrade pip \
#     && pip install virtualenv \
#     && virtualenv venv \
#     && source venv/bin/activate \
#     && pip install git+https://github.com/aleju/imgaug --no-deps \
#     && pip install -r requirements.txt    

CMD ["python","server.py"]
# CMD ["venv/bin/python","server.py"]
