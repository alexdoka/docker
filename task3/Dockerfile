FROM centos:7
LABEL AUTHOR=adakutovich
RUN yum install -y httpd web-assets-httpd && yum clean all
RUN echo "Student: aliaksandr dakutovich" > /var/www/html/index.html
EXPOSE 80
ENTRYPOINT ["httpd"]
CMD ["-DFOREGROUND"]

