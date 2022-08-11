FROM node

WORKDIR /app

COPY package.json /app/

RUN npm install

COPY . /app/

# default argument, this alone won't be recognized in the env variable, and it cannot used in runtime commands such as CMD
ARG DEFAULT_PORT=80

ENV PORT ${DEFAULT_PORT}

EXPOSE $PORT

# Add this to command line as -v /app/temp
# VOLUME ["/temp"]

# VOLLUME argument: path inside of container Note: this is an anonyomous volume
# VOLUME ["/app/node_mocules"]

CMD ["npm", "start"]