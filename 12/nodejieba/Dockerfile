FROM 12.13.0-buster-slim
MAINTAINER      xikakera "xikakera@gmail.com"

USER root
WORKDIR /
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
  && echo 'Asia/Shanghai' >/etc/timezone
RUN echo "deb http://mirrors.163.com/debian/ jessie main non-free contrib" >> /etc/apt/sources.list\
    && echo "deb http://mirrors.163.com/debian/ jessie-updates main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb http://mirrors.163.com/debian/ jessie-backports main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb-src http://mirrors.163.com/debian/ jessie main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb-src http://mirrors.163.com/debian/ jessie-updates main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb-src http://mirrors.163.com/debian/ jessie-backports main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb http://mirrors.163.com/debian-security/ jessie/updates main non-free contrib" >> /etc/apt/sources.list \
    && echo "deb-src http://mirrors.163.com/debian-security/ jessie/updates main non-free contrib" >> /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y g++ make

RUN npm config set registry https://registry.npm.taobao.org
RUN npm config set sass_binary_site http://cdn.npm.taobao.org/dist/node-sass
RUN npm config set disturl https://npm.taobao.org/dist

RUN npm install nodejieba