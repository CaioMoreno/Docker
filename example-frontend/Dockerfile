FROM node

WORKDIR /usr/src/app 

COPY package*.json ./

RUN npm install

EXPOSE 5000

COPY . .

ENV REACT_APP_BACKEND_URL=http://localhost:8080

RUN npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]
