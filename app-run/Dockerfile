FROM alpine:3.14
RUN apk update && apk add openjdk11-jre
RUN mkdir -p /opt/tomcat/webapps/
COPY --from=app-build /opt/tomcat /opt/tomcat/
VOLUME /opt/tomcat/webapps/
EXPOSE 8087
CMD ["/opt/tomcat/bin/catalina.sh", "run"]