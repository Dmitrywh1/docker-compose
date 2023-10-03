FROM alpine:3.14
RUN apk update && apk add openjdk11
RUN mkdir /opt/tomcat
COPY --from=build /opt/tomcat /opt/tomcat
ENV CATALINA_HOME /opt/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
RUN apk del --no-cache openjdk11-jre-headless
RUN rm -rf /var/cache/apk/*
RUN rm -rf $CATALINA_HOME/native-jni-lib/*
EXPOSE 8080
CMD ["catalina.sh", "run"]