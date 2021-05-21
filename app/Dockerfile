FROM node:12-alpine
RUN apk add --no-cache python g++ make
WORKDIR /app
# COPY . .
# RUN yarn install --production
COPY package.json yarn.lock ./
RUN yarn install --production
COPY . .
CMD ["node", "src/index.js"]
# FROM node:12 AS build
# WORKDIR /app
# COPY package* yarn.lock ./
# RUN yarn install
# COPY public ./public
# COPY src ./src
# RUN yarn run build

# FROM nginx:alpine
# COPY --from=build /app/build /usr/share/nginx/html