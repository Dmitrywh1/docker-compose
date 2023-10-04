FROM adoptopenjdk/openjdk11:alpine-jre
RUN mkdir /opt/tomcat && / rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/
COPY --from=build /opt/tomcat /opt/tomcat
ENV CATALINA_HOME /opt/tomcat && / PATH $CATALINA_HOME/bin:$PATH
EXPOSE 8080
CMD ["catalina.sh", "run"]