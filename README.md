# springcloud
select springboot and springcloud https://start.spring.io/actuator/info

服务器启动项目sh service.sh
firewall-cmd --zone=public --add-port=80/tcp --permanent
firewall-cmd  --reload
screen -R service java -jar ./*.jar

服务器debug项目 debugService.sh
ll-cmd --zone=public --add-port=8088/tcp --permanent
firewall-cmd  --reload
screen -R serviceDebug java  -jar -agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=8088 baogang-0.0.1-SNAPSHOT.jar
