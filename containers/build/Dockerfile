# Wybierz obraz bazowy z Node.js do budowania aplikacji
FROM node:14 

RUN apt-get update -y && \
    apt-get upgrade -y 
    #libavahi-compat-libdnssd-dev

RUN npm install yarn -y
#--network-concurrency 1 -y 

RUN git clone https://github.com/Patuuuska/web-app

# Ustaw katalog roboczy w kontenerze
WORKDIR /web-app

# Zainstaluj zależności
RUN yarn install

# Zbuduj aplikację w trybie produkcyjnym
RUN yarn build:prod

