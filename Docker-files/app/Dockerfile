FROM openjdk:11 AS base_image
RUN apt update && apt install maven -y
WORKDIR /code
RUN git clone https://github.com/Reeceakhun/Dockerizing-Java-Application.git
RUN cd Dockerizing-Java-Application && git checkout main && mvn install

FROM tomcat:9-jre11
RUN rm -rf /usr/local/webapps/*
COPY --from=base_image /target/vprofile-v2.war  /usr/local/webapps/ROOT.war

EXPOSE 8080
CMD ["catalina.sh", "run"]
