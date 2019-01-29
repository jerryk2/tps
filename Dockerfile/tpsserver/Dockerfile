FROM centos:7.5.1804

RUN mkdir /tftpboot

ADD dcsrd.repo /etc/yum.repos.d/dcsrd.repo
RUN yum -y install  tftp-server java-1.6.0-openjdk java-1.6.0-openjdk-devel
RUN yum clean all

ADD tpsserver-prod.service /etc/systemd/system/tpsserver-prod.service
ADD tpsserver-alpha.service /etc/systemd/system/tpsserver-alpha.service

RUN systemctl daemon-reload
RUN systemctl enable tpsserver-prod.service
RUN systemctl enable tpsserver-alpha.service

EXPOSE 9000
EXPOSE 9005
