FROM centos:7.5.1804

RUN mkdir /tftpboot
RUN yum -y install httpd
RUN yum clean all
RUN systemctl enable httpd.service

EXPOSE 80
