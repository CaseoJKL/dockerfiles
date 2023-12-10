FROM node:18.16.0-alpine3.17

# Make a directory for the app (/opt is a dir for application files)
RUN mkdir -p /opt/app

# Print the current working directory
RUN pwd

# Go to the newly created directory
WORKDIR /opt/app

# Print the current working directory again
RUN pwd

# Copy the contents of the build context to the app directory
# COPY . /opt/app

# Print the contents of the /opt/app directory
RUN ls -l /opt/app

COPY . .

# Install packages
RUN npm install

RUN npm i -g cross-env

RUN npm i @medusajs/medusa-cli

# Build project
RUN npm run build

# RUN rm -rf ./node_modules

# Copy files to the app directory
# COPY ./dist /opt/app
EXPOSE 9000

# RUN medusa migrations run

CMD [ "npm", "start" ]




