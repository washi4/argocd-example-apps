# 使用Go语言官方提供的Golang镜像作为基础镜像
FROM golang:1.16-alpine

# 设置工作目录
WORKDIR /app

# 复制Go模块文件并下载依赖
COPY go.mod ./
RUN go mod download

# 将代码复制到镜像中
COPY . .

# 构建Go应用
RUN go build -o main .

# 设置容器启动时运行的命令
CMD ["/app/main"]

# 暴露容器的端口
EXPOSE 8080
