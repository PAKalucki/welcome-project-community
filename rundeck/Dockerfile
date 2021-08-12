ARG RUNDECK_IMAGE
FROM ${RUNDECK_IMAGE}

RUN  sudo apt-get update && \
     sudo apt-get install -y -qq wget git curl jq iputils-ping sysstat python3-pip && \
     python3 -m pip install -U pip setuptools && \
     pip3 install ansible

COPY --chown=rundeck:root data/resources.yml /home/rundeck
COPY data/realm.properties /home/rundeck/server/config
COPY data/linux_id_rsa /home/rundeck
COPY data/plugins/. /home/rundeck/libext
COPY hosts /etc/ansible/hosts
COPY ansible.cfg /etc/ansible/ansible.cfg

ENV PATH="/home/rundeck/.local/bin:$PATH"