
FROM node:22-alpine

WORKDIR /app

ADD https://github.com/raghavendra89/ic-newsfeed-frontend.git .

ARG BACKEND_PORT

RUN sed -i 's/^VITE_LARAVEL_BACKEND_URL.*$/VITE_LARAVEL_BACKEND_URL=http:\/\/localhost:'"${BACKEND_PORT}"'/' .env

RUN npm install

# Install serve package
RUN npm i -g serve

RUN npm run build

EXPOSE 3000

CMD [ "serve", "-s", "dist" ]