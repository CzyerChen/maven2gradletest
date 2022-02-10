本项目为maven项目到gradle项目迁移的简单测试

## 步骤一 初始化Maven项目

通过[Maven Java项目脚手架](https://start.aliyun.com/bootstrap.html)初始化一个测试的maven项目，模拟现有的spring、springboot项目

## 步骤二 Maven项目迁移到Gradle项目

- 在项目根目录执行
- gradle init --type pom 
- 依照maven项目的pom进行迁移
- 使用gradle clean build -x test替代mvn clean package -Dmaven.test.skip=true
- 初次构建较耗时，二次构建就能比较快速
- 如果gradle构建较慢，考虑配置国内镜像