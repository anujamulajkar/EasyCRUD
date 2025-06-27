FROM maven:3.8.3-openjdk-17
COPY . /opt/
WORKDIR /opt 

#RUN rm -rf backend\src\main\resources\application.properties

#COPY application.properties backend\src\main\resources\application.properties

RUN mvn clean package -DskipTest

WORKDIR /opt/target/

EXPOSE 8080

ENTRYPOINT ["java", "-jar"]
CMD ["student-registration-backend 0.0.1-SNAPSHOT.jar"]

