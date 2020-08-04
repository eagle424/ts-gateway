FROM openjdk:8u201-jre-alpine

EXPOSE 8080

RUN    SPRING_OUTPUT_ANSI_ENABLED=ALWAYS \
    && JHIPSTER_SLEEP=0 \
    && JAVA_OPTS=" -Dspring.profiles.active=test -Dmaven.test.skip=true "
    && cd /home
    && cp entrypoint.sh entrypoint.sh
    && cp *.jar app.jar
    && chmod -R 755 .

# 复制文件
# ADD entrypoint.sh entrypoint.sh
# ADD *.jar app.jar

# 赋权限
# RUN chmod -R 755 .

ENTRYPOINT ["./entrypoint.sh"]