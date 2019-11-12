ARG CENTOS_VERSION
FROM centos:${CENTOS_VERSION}
ARG JAVA_VERSION=11
RUN yum install java-${JAVA_VERSION}-openjdk -y  && yum clean all
