#
# MAINTAINER        Kevin,S.Q.B <409747494@qq.com>
# DOCKER-VERSION    1.6.2
#
# Dockerizing Mariadb: Dockerfile for building Mariadb images
#
FROM shuimin/centos:7.1
MAINTAINER Kevin,S.Q.B <409747494@qq.com>

ENV DATA_DIR /var/lib/mysql

# Install Mariadb
RUN yum install -y mariadb mariadb-server && \
    yum clean all

ADD mysqld_charset.cnf /etc/my.cnf.d/

COPY scripts /scripts
RUN chmod +x /scripts/start

EXPOSE 3306

VOLUME ["/var/lib/mysql"]

ENTRYPOINT ["/scripts/start"]
