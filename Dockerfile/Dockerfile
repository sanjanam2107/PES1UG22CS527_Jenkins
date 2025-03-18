FROM jenkins/jenkins:lts

USER root

# Change Debian sources list to use a stable mirror
RUN echo "deb http://ftp.us.debian.org/debian bookworm main" > /etc/apt/sources.list && \
    echo "deb http://security.debian.org/debian-security bookworm-security main" >> /etc/apt/sources.list && \
    echo "deb http://ftp.us.debian.org/debian bookworm-updates main" >> /etc/apt/sources.list && \
    apt-get update && apt-get install -y make g++ --fix-missing

USER jenkins
