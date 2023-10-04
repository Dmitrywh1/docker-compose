FROM tomcat:9-jdk11-openjdk-slim
COPY --from=build /opt/tomcat/webapps/webapp.war $CATALINA_HOME/webapps/
EXPOSE 8080
CMD ["catalina.sh", "run"]