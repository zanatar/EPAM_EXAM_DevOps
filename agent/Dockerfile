FROM jenkins/ssh-agent:latest
RUN apt update&& apt install -y python3
RUN python -m pip install -U pip &&\
    pip install --upgrade pip &&\
	pip install ansible
