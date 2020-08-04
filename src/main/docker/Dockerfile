FROM openjdk:8u201-jre-alpine
# 暴露端口
EXPOSE 8080
# 设置目录
WORKDIR ~
# 复制
COPY entrypoint.sh entrypoint.sh
COPY *.jar app.jar
# 执行命令
RUN export SPRING_OUTPUT_ANSI_ENABLED=ALWAYS &&\
    export JHIPSTER_SLEEP=0 &&\
    export JAVA_OPTS=" -Dspring.profiles.active=test -Dmaven.test.skip=true " &&\
    mv *.jar app.jar &&\
    chmod -R 755 .

#
ENTRYPOINT ["./entrypoint.sh"]