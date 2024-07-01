FROM node:14

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . /app

EXPOSE 80

# 컨테이너의 외부폴더에 매핑되어질 내 컨테이너의 내부 위치 => 익명볼륨 
# VOLUME [ "/app/feedback" ] 

CMD ["node", "server.js"]

