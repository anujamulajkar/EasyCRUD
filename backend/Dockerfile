FROM maven:3.8.3-openjdk-17
COPY . /opt/
WORKDIR /opt 

RUN rm -rf backend\src\main\resources\application.properties

RUN cp -f  application.properties backend\src\main\resources\application.properties

RUN mvn clean package -DskipTests

WORKDIR /opt/target/

EXPOSE 8080

#ENTRYPOINT ["java", "-jar"]
CMD ["java", "-jar", "student-registration-backend-0.0.1-SNAPSHOT.jar"]

