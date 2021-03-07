FROM jenkins/ssh-agent:latest
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
RUN apt update&& apt install -y python3 python3-pip apt-transport-https ca-certificates curl software-properties-common docker-ce
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add 
RUN pip3 install ansible
RUN groupadd docker && usermod -aG docker jenkins
COPY jenkins_agent_key.pub /home/jenkins/.ssh/authorized_keys