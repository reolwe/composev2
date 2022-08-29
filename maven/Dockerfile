FROM ubuntu:20.04
ENV TZ=Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
RUN apt update
RUN apt install -y git
RUN apt install -y wget
RUN apt install -y default-jdk
RUN git clone https://github.com/reolwe/origin556.git
RUN apt install -y maven
WORKDIR /origin556/
RUN ls -l
RUN mvn clean
RUN mvn clean
RUN mvn install
RUN mkdir -p /origin556/config/
RUN cp /origin556/target/App42PaaS-Java-MySQL-Sample-0.0.1-SNAPSHOT/Config.properties /origin556/config

CMD ["mvn"]