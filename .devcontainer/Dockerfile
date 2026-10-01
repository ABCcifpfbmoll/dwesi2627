FROM eclipse-temurin:21-jdk-jammy

# Instal·lació de Tomcat 10, Git i utilitats bàsiques
ENV TOMCAT_VERSION 10.1.19
RUN apt-get update && apt-get install -y wget git curl openssh-server && \
    wget https://archive.apache.org/dist/tomcat/tomcat-10/v${TOMCAT_VERSION}/bin/apache-tomcat-${TOMCAT_VERSION}.tar.gz && \
    tar -xvf apache-tomcat-${TOMCAT_VERSION}.tar.gz -C /opt/ && \
    mv /opt/apache-tomcat-${TOMCAT_VERSION} /opt/tomcat && \
    rm apache-tomcat-${TOMCAT_VERSION}.tar.gz && \
    rm -rf /var/lib/apt/lists/*

ENV CATALINA_HOME /opt/tomcat
ENV PATH $CATALINA_HOME/bin:$PATH

EXPOSE 8080
