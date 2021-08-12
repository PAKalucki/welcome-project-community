FROM rundeck/node-demo

ENV LANG C.UTF-8
ENV LC_ALL C.UTF-8

RUN  sudo apt-get update && \
     sudo apt-get install -y -qq wget git curl jq iputils-ping sysstat python3-pip && \
     python3 -m pip install -U pip setuptools && \
     pip3 install ansible

#Add commands here to customize node-demo image.
#Adjust docker-compose to build from this file by replacing:
# image: rundeck/node-demo
# with
# build:
#   context: node-demo
