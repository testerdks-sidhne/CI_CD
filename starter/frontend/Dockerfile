FROM public.ecr.aws/docker/library/node:18.14.2-alpine3.17 as build

ARG REACT_APP_MOVIE_API_URL
ENV REACT_APP_MOVIE_API_URL=${REACT_APP_MOVIE_API_URL}

WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build

FROM public.ecr.aws/docker/library/node:18.14.2-alpine3.17
WORKDIR /app
COPY package*.json ./
RUN npm install -g serve
COPY --from=build /app/build ./build

EXPOSE 3000
CMD ["serve", "-s", "build", "-l", "3000"]