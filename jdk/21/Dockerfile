FROM alpine:3.21.2

# 设置语言环境变量为中文
ENV LANG=zh_CN.UTF-8

# 安装所需的软件包，包括中文字体和中文语言支持
RUN apk add --no-cache \
        ttf-dejavu \
        fontconfig \
        tzdata \
        openjdk21 \
        && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone

# 设置 JAVA_HOME 环境变量
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
