FROM ubuntu:latest
RUN apt-get update && apt-get upgrade -y
RUN apt-get update && apt-get install git -y
RUN apt-get update && apt-get install curl -y
RUN apt-get update && apt-get install apt-utils -y
RUN curl https://install.meteor.com/ | sh
RUN git clone https://github.com/RocketChat/Rocket.Chat.git
RUN meteor npm install --prefix Rocket.Chat/


