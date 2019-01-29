FROM centos:7.5.1804

ADD tftpd.map /etc/tftpd.map
ADD tftp /etc/xinetd.d/tftp

RUN mkdir /tftpboot
RUN yum -y install xinetd
RUN yum clean all

RUN systemctl enable xinetd.service

EXPOSE 69/udp
