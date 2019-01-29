FROM centos:7.5.1804

RUN mkdir /tftpboot
RUN yum -y install nfs-utils
RUN yum clean all
RUN systemctl enable nfs.service

EXPOSE 111
EXPOSE 111/udp
EXPOSE 2049
EXPOSE 2049/udp
EXPOSE 20048
EXPOSE 20048/udp
