FROM java:8-jdk

ENV WIREMOCK_VERSION 2.4.1

# download wiremock-standalone jar
RUN mkdir -p /opt/wiremock/ \
    && curl -sSL -o /opt/wiremock/wiremock-standalone.jar \
    http://repo1.maven.org/maven2/com/github/tomakehurst/wiremock-standalone/${WIREMOCK_VERSION}/wiremock-standalone-${WIREMOCK_VERSION}.jar

WORKDIR /home/wiremock

# COPY stubs /home/wiremock
# ADD extenstions /opt/wiremock/ext/

EXPOSE 8080 8081

# launch java from workdir
ENTRYPOINT ["java", "-cp", "/opt/wiremock/*:/opt/wiremock/ext/*", "com.github.tomakehurst.wiremock.standalone.WireMockServerRunner"]