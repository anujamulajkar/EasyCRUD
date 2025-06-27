FROM node:24-alpine

COPY . /opt/

WORKDIR /opt

RUN npm install && npm run build

RUN apk update && apk add apahce2 

EXPOSE 80

CMD ["apachectl","-DFOREGROUND"]

#ENTRYPOINT ["apachectl","-DFOREGROUND"]