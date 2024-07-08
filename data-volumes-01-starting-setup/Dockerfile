FROM node:14

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . /app

EXPOSE 80

# 컨테이너의 외부폴더에 매핑되어질 내 컨테이너의 내부 위치 => 익명볼륨 
# VOLUME [ "/app/feedback" ] 

 #docker run -d -p 3000:80 -v feedback:/app/feedback -v "C:\dev\study\docker\data-volumes-01-starting-setup:/app" -v /app/node_modules(이거 적는거랑 같은거임) feedback-node:v
# VOLUME [ "/app/node_modules" ] 

CMD ["npm", "start"]

