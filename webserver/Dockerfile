FROM centos:7
RUN yum -y install epel-release
RUN yum install -y git python3
RUN python3 -m pip install -U pip &&\
    pip install --upgrade pip
COPY student_exam2 student_exam2
WORKDIR student_exam2
ENV FLASK_APP=js_example
ENV LANG=en_US.utf8
CMD python3 -m venv venv && \
	. venv/bin/activate && \
	pip install -e . && \
    flask run --host=0.0.0.0