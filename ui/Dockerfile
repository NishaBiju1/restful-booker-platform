FROM node:6

ADD . /usr/local/ui

WORKDIR /usr/local/ui

RUN npm install
RUN npm rebuild node-sass --force
RUN npm install frontail -g
RUN touch ui.log

ENTRYPOINT sleep 5 && npm start & frontail -t dark -p 9003 ui.log
