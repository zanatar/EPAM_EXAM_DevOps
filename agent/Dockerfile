FROM jenkins/ssh-agent:latest
RUN apt update || apt install -y python3 python3-pip docker.io
RUN pip3 install ansible selinux
RUN ansible-galaxy collection install community.docker
COPY jenkins_agent_key.pub /home/jenkins/.ssh/authorized_keys
COPY setup.py setup.py
COPY README.rst README.rst
RUN pip3 install -e '.[test]'