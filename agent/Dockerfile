FROM jenkins/ssh-agent:latest
RUN apt update && \
	apt install -y software-properties-common && \
	add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable" && \
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add 
RUN apt update&& apt install -y python3 python3-pip apt-transport-https ca-certificates docker-ce
RUN pip3 install ansible
RUN groupadd docker && usermod -aG docker jenkins
COPY jenkins_agent_key.pub /home/jenkins/.ssh/authorized_keys