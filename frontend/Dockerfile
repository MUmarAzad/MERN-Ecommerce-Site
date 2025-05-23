FROM node:24-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

ARG REACT_APP_BASE_URL

ENV REACT_APP_BASE_URL=$REACT_APP_BASE_URL

# Increase Node.js memory limit during build
ENV NODE_OPTIONS=--max_old_space_size=4096

RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
