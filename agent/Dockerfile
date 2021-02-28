FROM jenkins/ssh-agent:latest
RUN apt update&& apt install -y python3 python3-pip
RUN pip3 install --upgrade pip3 &&\
	pip3 install ansible
