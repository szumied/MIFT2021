From ubuntu:latest

RUN apt-get update

RUN apt-get install -y git

RUN apt-get install -y default-jdk 

RUN apt-get install -y gradlew

Run cd ~

RUN git clone https://github.com/swimos/simple-chat.git

RUN cd simple-chat

RUN ./gradlew run



