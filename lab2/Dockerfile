FROM python:3.9-slim

RUN apt-get update && apt-get install -y \
    sshpass \
    openssh-client \
    nano

RUN python3 -m pip install ansible

WORKDIR /lab2

COPY . /lab2/

# Ansible ругается, если у private_key много прав
RUN chmod 600 /lab2/private_key