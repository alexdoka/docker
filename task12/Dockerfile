FROM ubuntu 
#COPY ./nginx.repo /etc/yum.repos.d/ 
RUN apt update -y
RUN apt install nginx -y
RUN echo "aliaksandrdakutovich/nginx:12-ubuntu" >  /var/www/html/index.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
#CMD ["-DFOREGROUND"]

