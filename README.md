# jaxrs-swagger-sample
Sample project for integrate swagger with jaxrs

生成api数据文件：

```shell script
$ mvn compile
```

使用docker提供swagger ui服务：

```shell script
# 拉取官方提供的ui服务镜像
$ docker pull swaggerapi/swagger-ui
# 启动一个容器，使用刚才生成的文件提供数据
$ docker run -itd -v ~/docker-share:/docker-share -e SWAGGER_JSON=/docker-share/swagger/jaxrs-api.json -p 8081:8080 swaggerapi/swagger-ui
```