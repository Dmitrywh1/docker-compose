FROM tomcat
RUN apt-get update
RUN apt install openjdk-11-jdk -y
COPY --from=app-build /opt/tomcat /home/dmitry/lesson/docker-compose/tomcat/
ENV CATALINA_HOME /opt/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
EXPOSE 8080
CMD ["catalina.sh", "run"]

