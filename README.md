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



授权
gradle release -Prelease.customUsername=**** -Prelease.customPassword=****

https://axion-release-plugin.readthedocs.io/en/latest/configuration/authorization/
```



在USER_HOME/.gradle目录的gradle.properties里维护自定义属性