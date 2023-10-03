FROM ubuntu:18.04
RUN apt-get update
RUN apt install openjdk-11-jdk -y
ENV CATALINA_HOME /opt/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
EXPOSE 8080
CMD ["catalina.sh", "run"]

