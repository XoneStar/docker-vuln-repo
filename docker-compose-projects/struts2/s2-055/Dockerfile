FROM vulhub/tomcat:8.5

MAINTAINER phithon <root@leavesongs.com>

RUN set -ex \
    && rm -rf /usr/local/tomcat/webapps/* \
    && chmod a+x /usr/local/tomcat/bin/*.sh

ADD struts2-rest-showcase.war /usr/local/tomcat/webapps/
EXPOSE 8080