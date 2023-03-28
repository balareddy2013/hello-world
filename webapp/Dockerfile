# Pull base image 
FROM ubuntu:latest
RUN apt-get update
RUN apt-get update && apt-get install -y openjdk-17-jdk
ENV JAVA_HOME="/usr/lib/jvm/java-17-openjdk-amd64"
RUN apt install tomcat9 tomcat9-admin
# Maintainer 
COPY ./target/webapp.war /usr/local/tomcat/webapps
EXPOSE 9000
CMD ["catalina.sh", "run"]
