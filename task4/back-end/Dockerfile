FROM ubuntu:latest

RUN apt-get update
RUN apt-get upgrade -y

RUN apt install -y python3 python3-pip

RUN rm /usr/lib/python*/EXTERNALLY-MANAGED
RUN pip install flask
RUN pip install flask-cors

WORKDIR /app

COPY api.py ./

CMD ["python3", "api.py"]
