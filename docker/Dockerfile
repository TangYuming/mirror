# mirrord's Dockerfile

FROM debian
MAINTAINER felinae <fellinae@qq.com>

RUN apt-get update
RUN apt-get install -y rsync python-pip

RUN pip install mirror

RUN mkdir /var/log/mirrord /var/log/rsync /mirror
VOLUME ["/mirror", "/var/log"]

ENTRYPOINT ["mirrord", "-c /etc/mirror/mirror.ini"]
