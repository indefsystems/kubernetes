#multi-step docker file
# builder phase - purpose of this phase is to install the dependecies and build the application
FROM node:alpine as builder

WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

# output from above npm build process is a build folder created in working directory
# /app/build - all the production assets are here

FROM nginx
EXPOSE 80

# copy from the builder phase
COPY --from=builder /app/build /usr/share/nginx/html
