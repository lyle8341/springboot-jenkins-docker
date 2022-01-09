# springboot-jenkins-docker
springboot-jenkins-docker



### axion-release
```
$ git tag
<empty list>

$ gradle currentVersion
Project version: 0.1.0-SNAPSHOT


$ gradle release
$ git tag
release-0.1.0



授权(命令行方式)
gradle release -Prelease.customUsername=**** -Prelease.customPassword=****

https://axion-release-plugin.readthedocs.io/en/latest/configuration/authorization/
```

+ Could not find method leftShift() for arguments 
  ```
  << was deprecated in Gradle 4.x and removed in Gradle 5.0
  ```

+ 敏感参数key在本地保存
  - 在USER_HOME/.gradle目录的gradle.properties里维护自定义属性
    ```
    customerUsername=lyle8341
    customerPassword=token....
    ```

## 一定要有新提交内容且推送到远端才可以，release，！！！！

+ 1.打包
  + gradle app:clean app:bootJar
+ 2.制作镜像
  ```shell
  # 点表示当前目录（Dockerfile的路径）
  docker build -t jenkens-demo:0.1.1 .
  # -t : Name and optionally a tag in the 'name:tag' format
  ```
+ 3.查看镜像构建过程
  + docker history jenkens-demo:0.1.1
+ 4.清理 build cache 可选
  + docker builder prune
+ 5.本地测试
  + docker run --rm -p 8080:8080 jenkens-demo:0.1.1