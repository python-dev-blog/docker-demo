FROM python:3.8.10-slim

RUN mkdir docker_demo
WORKDIR docker_demo

ADD requirements.txt /docker_demo/
RUN pip install -r requirements.txt
ADD . /docker_demo/

ADD .docker.env /docker_demo/.env
ENV APP_NAME=DOCKER_DEMO

RUN pip3 install -r requirements.txt


CMD gunicorn docker_demo.wsgi:application -b 0.0.0.0:8000