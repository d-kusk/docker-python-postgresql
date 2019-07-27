FROM python:3.7.2

ENV PYTHONUNBUFFERED 1

RUN mkdir /code
WORKDIR /code

ADD requirements_default.txt /code/
RUN pip install --upgrade pip && \
    pip install -r requirements_default.txt

ADD . /code/
