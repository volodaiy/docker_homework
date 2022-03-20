FROM node:14-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
RUN npm install -g serve
COPY . .
ENV PORT=80
RUN npm run build
EXPOSE 80
CMD [ "serve", "-s", "build", "-l", "80" ]