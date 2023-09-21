# Use an official Node.js 18 image as the base image
FROM node:18-alpine

WORKDIR /app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

EXPOSE 1000

RUN npm install

# If you are building your code for production
#RUN npm ci --omit=dev
RUN npm ci 

# Bundle app source
COPY . .
EXPOSE 8080
CMD [ "node", "index.js" ]