FROM centos:7.5.1804

ADD smb.conf /etc/samba/smb.conf

RUN mkdir /tftpboot
RUN yum -y install samba
RUN yum clean all
RUN systemctl enable smb.service

EXPOSE 139
