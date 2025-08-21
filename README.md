# Java-Boot-Template

Spring-Boot 模板项目，助力项目快速启动，包含以下功能：

- spring-boot: 2.3.6
- lombok
- mapstruct
- mybatis-plus
- redis
- 极致的分页查询
- ip 获取，ip2region
- 对象存储，腾讯 cos
- 登录、注册、验证码、用户

### Contributor

[Contributors](https://github.com/lijunping365/Java-Boot-Template/graphs/contributors)

## LICENSE

[Apache License](./LICENSE)


# 快速开始测试，脚手架是否正常
- 判断是Gradle还是Maven项目，看有没有pom.xml文件
找到main中的入口文件，启动后，拿到一个springBoot的脚手架后
## 启动报错如下：
java: java.lang.IllegalAccessError: class lombok.javac.apt.LombokProcessor (in unnamed module @0x7a8aaa33) 
cannot access class com.sun.tools.javac.processing.JavacProcessingEnvironment (in module jdk.compiler) because module jdk.compiler does not export com.sun.tools.javac.processing to unnamed module @0x7a8aaa33

### 解决方法
你的错误一般出现在 老版本 Lombok + 新版本 JDK。
•	Lombok 1.18.22+ 已经兼容 JDK 17。
•	如果你在 JDK 21 上，建议用最新的 Lombok（至少 1.18.30）。

#### 解决方案1：
JDK降级，使用JDK1.8，也就是java8；


## 第一步：查看当前的java项目的jdk版本
通过IDE工具，打开项目工具后，修改JDK版本
- 可以在项目结构中，修改JDK版本

## 第二步：查看当前的java项目的数据库
通过IDE工具，打开项目工具后，修改数据库连接信息
打开文件：配置文件，application-dev，修改数据库连接信息
账号密码正确即可。

## 第三步：再次启动项目
一般会发现成功。
找到接口访问即可。
```
server:
  port: 8080
  servlet:
    context-path: /boot-api

```


# 增加脚手架模块：swagger
