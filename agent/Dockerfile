FROM jenkins/ssh-agent:latest
# RUN apt update 
RUN	apt install -y apt-transport-https ca-certificates gnupg
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
	echo \
		"deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian \
		$(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
RUN apt update && apt install -y python3 python3-pip docker-ce docker-ce-cli containerd.io
RUN pip3 install ansible
RUN groupadd docker && usermod -aG docker jenkins
COPY jenkins_agent_key.pub /home/jenkins/.ssh/authorized_keys