FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

#Susbstitute with your ip
ENV IP_ADDRESS=192.168.1.228
EXPOSE 3000

CMD [ "npm", "start" ]
