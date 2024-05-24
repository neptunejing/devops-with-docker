FROM --platform=linux/amd64 node:16-alpine

WORKDIR /app

# copy package.json and package-lock.json to WORKDIR
COPY package*.json ./

RUN npm install

# copy the project
COPY . .

# build
RUN npm run build

EXPOSE 8080

# 启动应用
CMD ["npm", "run", "preview"]

