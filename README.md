

#微服务刷新
curl -X POST http://lxdyun.com:8400/refresh


#swagger 
http://localhost:8400/swagger-ui.html



#网关zuul  
类似于面向对象设计模式中的Facade模式， 它的存在就像是整个微服务架构系统的门面一样，所有的外部客户端访问都需要经过它来进行调度和过滤。
它除了要实现请求路由、 负载均衡、 校验过滤等功能之外， 还需要更多能力， 比如与服务治理框架的结合、 请求转发时的熔断机制、 服务的聚合等一系列高级功能。将自身注册为Eureka服务治理下的应用， 同时从Eureka中获得了所有其他微服务的实例信息。 这样的设计非常巧妙地将服务治理体系中维护的实例信息利用起来， 使得将维护服务实例的工作交给了服务治理框架自动完成， 不再需要人工介入。
1、用户登录状态token
2、签名校验的机制（为了防止客户端在发起请求时被篡改等安全方面的考虑）



spring-cloud 微服务组件demo



**工程名**	**描述**	**端口**
zipkin-server 链路追踪 9411
config-server	配置管理中心	8402
eureka-server	服务发现与注册中心	8404
hystrix-dashboard	监控	

api-gateway	服务网关	8401
autobot-res	ADC 	8400

常用命令：
本地仓库 的更新
mvn -X  clean package install 
远程 仓库 的更新
mvn clean package deploy
打包
mvn package

xmls阿里云不挂断运行命令 nohup java -jar XXX.jar & 
1. 查看端口号占用情况：netstat -apn|grep 80 (ESTABLISHED6426/lighttpd)
2. 确定进程号: ps -aux|grep <进程号> 
3. 杀掉该进程 : kill -9 

