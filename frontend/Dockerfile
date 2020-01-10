#Docker file for apache for demoapp
FROM centos:7
MAINTAINER waqaryshaikh@gmail.com
RUN yum -y update
#ADD scripts /opt
#RUN chmode 755 /opt/*
#RUN /opt/packages
RUN yum -y install httpd php php-gd php-mysql
ADD code /var/www/html
#COPY code/* /var/www/html
ENV MY_DB_HOST_WRITE=test
EXPOSE 80
#In case of multiple CMD only the last CMD command will run, rest will be overridden
#Alternate to CMD is ENTRYPOINT
CMD ["httpd", "-D", "FOREGROUND"]