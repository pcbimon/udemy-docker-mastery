FROM node:6-alpine
# install tini
RUN apk add --no-cache tini
# expose port 3000
EXPOSE 3000
# create app directory
RUN mkdir -p /usr/src/app
# set working directory
WORKDIR /usr/src/app
# copy all files from current directory to docker
COPY . .
# install all dependencies
RUN npm install
# remove cache
RUN npm cache clean --force
# run the app
CMD ["/sbin/tini", "--", "node", "./bin/www"]