FROM mcr.microsoft.com/devcontainers/base:jammy

RUN curl -sL https://deb.nodesource.com/setup_18.x | bash

RUN apt-get update && \
    apt-get -y install nodejs && \
    apt-get clean

# Install OpenJDK 18
RUN apt-get update && \
    apt-get -y install openjdk-18-jdk && \
    apt-get clean

# Verify Java installation
RUN java -version

# Install Maven for Spring Boot
RUN apt-get update && \
    apt-get -y install maven && \
    apt-get clean

# Set JAVA_HOME environment variable
ENV JAVA_HOME /usr/lib/jvm/java-18-openjdk-amd64
ENV PATH $PATH:$JAVA_HOME/bin

# # Create app directory
# WORKDIR /app

# # Copy backend directory contents
# COPY showcase-backend/.mvn/ ./backend/.mvn/
# COPY showcase-backend/mvnw backend/pom.xml ./backend/
# COPY showcase-backend/src ./backend/src

# # Set working directory to backend
# WORKDIR /app/backend