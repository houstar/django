FROM python:2.7
RUN mkdir /code
WORKDIR /code
ADD ./git_work.py /code/
RUN apt-get update -y && \
	apt-get install git python-mysqldb -y && \
	pip install MySQL-python && \
	apt-get clean
CMD python /code/git_work.py
