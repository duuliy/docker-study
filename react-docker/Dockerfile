# 使用node版本11.12.0
FROM node:11.12.0

# 代表生产环境
# ENV PROJECT_ENV production
# # 许多 package 会根据此环境变量，做出不同的行为
# # 另外，在 webpack 中打包也会根据此环境变量做出优化，但是 create-react-app 在打包时会写死该环境变量
# ENV NODE_ENV production
# 进入code文件夹，如果没有则会生成，并进入文件夹
# WORKDIR /react-docker
# # # 将当前内容 放入code文件夹
# COPY . /react-docker/dist

# 执行指令
RUN npm install && npm run build && npm install -g http-server

WORKDIR /react-docker/dist
COPY . /react-docker/dist

# 暴露容器端口 8080
EXPOSE 8080

# 当执行docker run的时候会执行以下shell 脚本。
CMD npx http-server ./dist