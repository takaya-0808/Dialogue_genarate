FROM python:3.8
USER root

RUN apt-get update && \
    apt-get upgrade
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8

RUN pip install --upgrade pip
RUN pip install --upgrade setuptools

ADD . /work
WORKDIR /work
RUN pip install -r requirements.txt
