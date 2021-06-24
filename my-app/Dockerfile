FROM tomcat:latest
LABEL maintainer="himanshu Jain"
ADD ./target/my-app-1.0-SNAPSHOT.jar /usr/local/tomcat/webapps/
EXPOSE 8080
CMD ["catalina.sh", "run"]
