FROM openjdk:8u131-jre-alpine

ENV SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    JHIPSTER_SLEEP=0 \
    JAVA_OPTS=" -Dspring.profiles.active=test "

WORKDIR /home

RUN pwd

# 复制文件
ADD entrypoint.sh entrypoint.sh
ADD *.jar app.jar

# 赋权限
RUN chmod -R 755 .

EXPOSE 8080

ENTRYPOINT ["./entrypoint.sh"]