FROM benhall/dind-jenkins-agent
RUN apt update || apt install -y python3-pip
RUN python -m pip install -U pip && \
	pip3 install ansible
COPY jenkins_agent_key.pub /home/jenkins/.ssh/authorized_keys