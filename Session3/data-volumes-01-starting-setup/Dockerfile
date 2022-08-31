FROM node:14

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

ARG DEFAULT_PORT=80

ENV PORT $DEFAULT_PORT

EXPOSE $PORT
# VOLUME [ "/app/node_modules" ]

# 익명 볼륨을 사용함으로서 바인드 마운트의 ro 옵션에서 제외(더 긴 경로이므로)
# 익명 볼륨을 사용함으로써 도커가 관리해야하는 영역을 실제 로컬 호스트 파일 시스템으로 돌려 효율을 올릴 수 있다.
# VOLUME ["/app/temp"]

CMD ["npm", "start"]