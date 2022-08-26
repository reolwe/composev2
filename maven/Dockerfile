FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt update
RUN apt install -y git
RUN apt install -y wget
RUN apt install -y default-jdk
RUN git clone https://github.com/reolwe/origin556.git
RUN apt install -y maven
WORKDIR /App42PaaS-Java-MySQL-Sample/
RUN ls -l
RUN mvn clean
RUN mvn install
CMD ["mvn"]