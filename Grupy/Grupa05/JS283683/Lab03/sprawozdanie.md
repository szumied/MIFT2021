0. Wstępnie naprawiano repozytorium po błędach występujących po wykonaniu pulla.

1. stworzono osobistego brancha: git checkout -b Grupa05-JS283683_Lab03

2. Skopiowano do .git/hooks/ kod git hooka sporzadzony w czasie poprzednich zajęć

3. Instalacja dockera odbyła się już wcześniej na używanej maszynie (w ubuntu-based dystrybucjach linuxa można bezproblemowo wykorzystać `sudo apt-get update; sudo apt install`, do wykonania tej instalacji)

4. Konto w hub.docker.com również było wczesniej przygotowane. Na maszynie trzeba było zalogować się do niego w terminalu poprzez polecenie `docker login`, aby móc pobierać gotowe obrazy.

5. Przygotowano dockerfile, który służył do zbudowania obrazu komendą `sudo docker build . -t devops-lab03`
sprawdzono, czy obraz się zbudował i jest dostępny poleceniem `sudo docker image ls` (alias `docker images`)
Treść pliku Dockerfile:
```
FROM ubuntu:latest
RUN apt-get -y update
RUN apt-get -y upgrade
RUN apt-get install -y build-essential
RUN apt-get install git -y
RUN cd ~
RUN git clone https://github.com/InzynieriaOprogramowaniaAGH/MIFT2021
RUN cd MIFT2021; git checkout Grupa05-JS283683_Lab03
```

6. Sprawdzono, czy przygotowany kontener zawiera gałąź roboczą.
`sudo docker ps`
`sudo docker run -it devops-lab03`
`cd MIFT2021; git branch`


Końcowo sporządzono sprawozdanie, wykonano sekwencję poleceń status-add-commit-pull-merge-push. 