FROM node:12

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . /app

# EXPOSE는 kubernetes cluster 안에서 노드끼리 통신하기 위해 명시해주는 PORT
# 외부 HOST port와 연동하기 위해서는 -publish (-p) HOST PORT: CONTAINER PORT 를 명시...
EXPOSE 80  

CMD ["node", "server.js"]