# Redis image for dev
# Version 1.0

# 基础镜像 最新的 redis alpine
FROM redis:6-alpine

# 维护者信息
LABEL maintainer="mambahj24@gmail.com"

# 镜像操作命令
RUN apt-get update && apt-get install vim -y && apt-get clean

# 暴露端口
EXPOSE 6379

# docker run --name spredis -p 6699:6379 -d --restart=always meredis:v1 redis-server --appendonly yes --requirepass "180234sss"