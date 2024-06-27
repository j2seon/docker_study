FROM node

# 실행되어야하는 폴더의 위치를 지정할수있다.
WORKDIR /app

# package.json을 저장함
COPY package.json /app

#노드 종속을 위해서 npm install 해야함
# 이미지에 해당 내용을 실행하고 싶다고 알리고 싶은 상황 /app 폴더에서 실행해야겠지?
RUN npm install

# 이미지를 만들거야
# COPY 복사되어야할 파일들이 있는곳(해당폴더~하위까지 이미지로만들어야해)  파일을 저장해야하는 이미지 내부경로
# COPY . /app
# 위에 WORKDIR 에서 작업 폴더를 지정하면 해당폴더가 루트 디렉토리가 된다.
# 따라서 copy에서 /app 이라 안적고 ./ 라고 적으면 /app으로 인식 
# 원하는 방법대로 /app 이라는 절대경로를 사용해도되고 상대경로를 사용해도된다.
COPY . /app


# 시스템에 특정포트를 노출해야 접근이 가능
EXPOSE 80 

#CMD : 이미지가 생성될때 실행되지 않고 이미지 기반으로 컨테이너가 시작될때 실행된다. 
CMD ["node", "server.js"]

# docker run으로 실행시킬때 -p로 포트를 열어줘야한다.
# docker run -p 접근하려는 로컬 포트 도커의 내부포트
# docker run -p 3000:80 8a5a65a4c2edfb750b20f7c6a898fa2d5e98dc4a394e59680f06adecca773d10