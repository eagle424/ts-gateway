FROM openjdk:8u201-jre-alpine

EXPOSE 8080

WORKDIR /home

RUN export SPRING_OUTPUT_ANSI_ENABLED=ALWAYS && \
    export JHIPSTER_SLEEP=0 && \
    export JAVA_OPTS=" -Dspring.profiles.active=test -Dmaven.test.skip=true "
RUN cp entrypoint.sh entrypoint.sh

RUN cp *.jar app.jar && \
    chmod -R 755 .

# 复制文件
# ADD entrypoint.sh entrypoint.sh
# ADD *.jar app.jar

# 赋权限
# RUN chmod -R 755 .

ENTRYPOINT ["./entrypoint.sh"]