FROM alpine:3.14
RUN mkdir /opt/tomcat
COPY --from=build /opt/tomcat /opt/tomcat
ENV CATALINA_HOME /opt/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH
EXPOSE 8080
CMD ["catalina.sh", "run"]