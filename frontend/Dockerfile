FROM node:16-alpine

WORKDIR /app


COPY package*.json ./
RUN npm install

COPY . .
RUN npm run build

RUN npm install -g serve

EXPOSE 8000

CMD ["serve", "-s", "build", "--listen", "8000"]



