FROM node:24-alpine
WORKDIR /
COPY package*.json ./
RUN npm install
COPY . .

ARG MONGO_URL
ARG SECRET_KEY

ENV MONGO_URL=$MONGO_URL
ENV MSECRET_KEY=$SECRET_KEY

EXPOSE 5000

CMD ["npm", "run", "start"] 