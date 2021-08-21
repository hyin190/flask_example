FROM python:3.8

ENV PORT 8080
ENV HOST 0.0.0.0

EXPOSE 8080

RUN apt-get update -y && \
    apt-get install -y python3-pip

COPY ./requirements.txt /hello_world/requirements.txt

WORKDIR /main

RUN pip install -r requirements.txt

COPY . /main


ENTRYPOINT ["python", "main.py"]