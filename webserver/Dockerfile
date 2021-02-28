FROM centos:7
#RUN yum install -y epel-release
RUN yum install -y git python3
RUN python -m pip install -U pip
RUN git clone https://github.com/merovigen/student-exam2
WORKDIR student-exam2
ENV FLASK_APP=js_example
RUN python3 -m venv venv && \
	. venv/bin/activate && \
	pip install -e .
CMD flask run