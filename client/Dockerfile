FROM node:22.14.0 AS base

WORKDIR /app

COPY package*.json ./

RUN npm install --silent


FROM node:20-alpine

WORKDIR /app

COPY --from=base . .

EXPOSE 3000

ENTRYPOINT ["npm"]

CMD ["start"]