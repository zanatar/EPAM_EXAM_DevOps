FROM jenkins/ssh-agent:latest
RUN apt update || apt install -y python3 python3-pip libselinux-python3 docker.io
RUN pip3 install ansible
COPY jenkins_agent_key.pub /home/jenkins/.ssh/authorized_keys