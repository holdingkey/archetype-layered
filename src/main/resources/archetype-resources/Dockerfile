FROM --platform=linux/amd64 openjdk:8

# 设定时区
ENV TZ=Asia/Shanghai
RUN set -eux; \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime; \
    echo $TZ > /etc/timezone

ADD target/*.jar /app.jar

ENTRYPOINT ["java", "-jar", "/app.jar"]