FROM node:boron

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY package.json .
# For npm@5 or later, copy package-lock.json as well
# COPY package.json package-lock.json ./

RUN npm install

# Bundle app source
COPY . .

# Map app's bound port to docker daemon
EXPOSE 8080

CMD [ "npm", "start" ]


# TO RUN:
#
# *replace container id in exec command
# docker build -t cterrill/node-web-app .
# docker exec -it <container-id> /bin/bash
# docker run -p 49160:8080 -d cterrill/node-web-app
