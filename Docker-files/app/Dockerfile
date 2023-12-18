FROM openjdk:11 AS base_image
RUN apt update && apt install maven -y
WORKDIR /code
RUN git clone https://github.com/Reeceakhun/Dockerizing-Java-Application.git
RUN cd Dockerizing-Java-Application && git checkout main && mvn install
#RUN git clone https://github.com/devopshydclub/vprofile-project.git
#RUN cd vprofile-project && git checkout docker && mvn install
FROM tomcat:9-jre11
RUN rm -rf /usr/local/tomcat/webapps/*
COPY --from=base_image /code/Dockerizing-Java-Application/target/vprofile-v2.war  /usr/local/tomcat/webapps/ROOT.war
#COPY --from=base_image vprofile-project/target/vprofilr-v2.war /usr/local/tomcat/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]
