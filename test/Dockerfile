# 使用node版本11.12.0
FROM node:11.12.0

WORKDIR /test
COPY . /test

# 执行指令
RUN npm install -g http-server

# 暴露容器端口 8080
EXPOSE 8080

# 当执行docker run的时候会执行以下shell 脚本。
CMD npx http-server ./gg