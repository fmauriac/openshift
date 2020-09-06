FROM alpine
RUN apk update && apk upgrade
RUN apk add python3
RUN mkdir -p /opt/headlines
COPY src /opt/headlines
RUN pip3 install -r /opt/headlines/requirements.txt
WORKDIR /opt/headlines
ENTRYPOINT export FLASK_APP=headlines.py flask run --host=0.0.0.0 --port=8080
