FROM alpine 
COPY default.conf /etc/nginx/conf.d/ 
RUN mkdir /run/nginx/
RUN apk update 
RUN apk add nginx
RUN echo "aliaksandrdakutovich/nginx:13-alpine" >  /home/index.html
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
#CMD ["-DFOREGROUND"]

