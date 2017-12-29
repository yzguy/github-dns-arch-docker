FROM centos:7

RUN yum install -y epel-release && yum install -y nsd && yum clean all

COPY root /

RUN /sbin/nsd-checkconf /etc/nsd/nsd.conf

EXPOSE 53/tcp 53/udp

CMD /usr/sbin/nsd -d -c /etc/nsd/nsd.conf
