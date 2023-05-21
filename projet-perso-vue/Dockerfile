FROM node:10-alpine as builder

WORKDIR /app

# Copy the package.json and install dependencies
npm i -g npm@latest
COPY package*.json ./
# Run with latest version of npm to avoid lockfile v2 warning
RUN npm i npm@latest

# Copy all files
COPY . .

VOLUME /app
EXPOSE 8080
CMD ["npm", "run", "serve"]
