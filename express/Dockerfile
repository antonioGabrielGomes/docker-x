FROM node:16-alpine as base

WORKDIR /src
COPY package*.json /
EXPOSE 3333

FROM base as production
ENV NODE_ENV=production
RUN npm ci
COPY . /
CMD ["npm", "start"]
 