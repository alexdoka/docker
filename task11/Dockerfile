FROM centos:7
COPY ./nginx.repo /etc/yum.repos.d/ 
RUN yum install -y nginx  && yum clean all
RUN echo "aliaksandrdakutovich/nginx:11-centos" >  /usr/share/nginx/html/index.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
#CMD ["-DFOREGROUND"]

