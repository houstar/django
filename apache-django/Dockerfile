FROM python:2.7
ENV PYTHONUNBUFFERED 1

RUN pip install \
django==1.5.12 \
MySQL-python \
django-xadmin \
django-crispy-forms && \
apt-get update -y && \
apt-get install -y apache2 libapache2-mod-wsgi && \ 
apt-get clean 
ADD ./mysite /var/www/
ADD mysite-conf /etc/apache2/sites-available/

CMD /usr/sbin/apache2ctl -D FOREGROUND
