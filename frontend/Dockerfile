FROM node:24-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

ARG REACT_APP_BASE_URL

ENV REACT_APP_BASE_URL=$REACT_APP_BASE_URL

RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
