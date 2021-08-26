FROM node:14
RUN node -v && npm -v

EXPOSE 5000
ENV REACT_APP_BACKEND_URL=http://localhost:8080
WORKDIR /usr/src/app
COPY . .

RUN npm install
RUN npm install -g serve
RUN npm run build

CMD ["serve", "-s", "-l", "5000", "build"]
