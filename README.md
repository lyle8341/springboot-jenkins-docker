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