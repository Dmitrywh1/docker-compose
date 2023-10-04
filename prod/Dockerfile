FROM alpine:latest
RUN apk update && apk add openjdk11
RUN mkdir /opt/tomcat
COPY --from=build /opt/tomcat /opt/tomcat
ENV CATALINA_HOME /opt/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
RUN apk del --no-cache openjdk11-jre-headless && \
apk add --no-cache openjdk11 && \
apk del openjdk11-doc openjdk11-src openjdk11-demos
EXPOSE 8080
CMD ["catalina.sh", "run"]