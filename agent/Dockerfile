FROM jenkins/ssh-agent:latest
RUN apt update&& apt install -y python3 python3-pip
RUN pip3 install ansible
COPY jenkins_agent_key.pub /home/jenkins/.ssh/jenkins_agent_key.pub