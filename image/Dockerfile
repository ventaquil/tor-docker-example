FROM node

RUN apt-get update && \
        apt-get install -y tor vim

COPY entrypoint /sbin/entrypoint

WORKDIR /app

RUN npm install --save express

COPY index.js index.js

EXPOSE 8080

COPY torrc /etc/tor/torrc

CMD ["entrypoint"]

