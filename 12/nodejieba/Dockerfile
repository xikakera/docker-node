FROM node:12.13.0-buster-slim
MAINTAINER      xikakera "xikakera@gmail.com"

USER root
WORKDIR /
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
  && echo 'Asia/Shanghai' >/etc/timezone

RUN apt-get update
RUN apt-get install -y python-minimal

RUN npm install nodejieba