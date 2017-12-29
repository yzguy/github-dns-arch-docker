FROM centos:7

RUN yum install -y unbound && yum clean all

COPY root /

RUN /sbin/unbound-checkconf /etc/unbound/unbound.conf

EXPOSE 53/tcp 53/udp

CMD /usr/sbin/unbound -d
