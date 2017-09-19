#基于那个镜像
FROM java:8
VOLUME /tmp
ADD wget https://github.com/ykkxdu/docker-eureka-server.git app.jar
RUN bash -c 'touch /app.jar'
#声明需要暴露的端口
EXPOSE 8672
#容器时启动时执行此命令 java.security.egd=file:/dev/./urandom 为tomcat启动优化项
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]