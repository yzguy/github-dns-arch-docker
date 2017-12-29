FROM centos:7

RUN yum install -y epel-release yum-plugin-priorities && \
    curl -o /etc/yum.repos.d/powerdns-auth-41.repo https://repo.powerdns.com/repo-files/centos-auth-41.repo && \
    yum install -y pdns pdns-tools pdns-backend-postgresql && \
    yum clean all

COPY root /

EXPOSE 53/tcp 53/udp

CMD /usr/sbin/pdns_server --daemon=no --guardian=no --loglevel=9
