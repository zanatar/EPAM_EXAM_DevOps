FROM benhall/dind-jenkins-agent
RUN apt update || apt install -y python3 python3-pip
RUN python3 -m pip install -U pip && pip install ansible
COPY jenkins_agent_key.pub /home/jenkins/.ssh/authorized_keys