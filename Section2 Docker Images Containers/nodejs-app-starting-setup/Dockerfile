# Get images from local env or docker hub
# FROM node
FROM node:12

# Specify working directory, and tell docker subsequent command to excute in this folder
WORKDIR /app

# Specify which local file go to docker image, copy all files to image/app
# Since we already specify WORKDIR we can also do COPY . ./
# COPY . /app

# Optimization when rebuild
COPY package.json /app

# RUN npm install
RUN npm install

COPY . /app

# Since application is running on port 80, docker will isolate connection, speify EXPOSE for outside world to get access
# EXPOSE 80 is for documentation only, really doesn't do anything
EXPOSE 80

# CMD runs when container starts, should always be the last command in Dockerfile
# RUN vs CMD: RUN execute while building image, CMD runs after container starts
CMD ["node", "server.js"]