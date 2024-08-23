FROM node:20-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install --only=production

COPY . .

RUN npm install --save-dev @nestjs/cli

RUN npx nest build

EXPOSE 4000

CMD ["node", "dist/main.js"]