FROM tomcat:9.0.8-jre8-alpine
COPY --from=build /opt/tomcat/webapps/webapp.war /usr/local/tomcat/webapps
ENV CATALINA_HOME /usr/local/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
EXPOSE 8080
CMD ["catalina.sh", "run"]