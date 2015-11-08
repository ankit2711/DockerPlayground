FROM ankit2711/ubuntu

MAINTAINER Ankit Kumar <ak.ankitkumar@gmail.com>

# Add oracle java 8 repository
RUN apt-get -y install software-properties-common
RUN add-apt-repository ppa:webupd8team/java
RUN apt-get -y update
# Accept the Oracle Java license
RUN echo "oracle-java8-installer shared/accepted-oracle-license-v1-1 boolean true" | debconf-set-selections
# Install Oracle Java
RUN apt-get -y install oracle-java8-installer

ENV JAVA_HOME /usr/lib/jvm/java-8-oracle
