## 使用说明
目前的logstash.conf支持tomcat访问日志、启动日志以及符合以下约定的应用日志收集。

为了收集日志，还需要在每台机器上部署个filebeat，把日志目录映射到filebeat容器中，
通过filebeat向logstash发送日志。

1. 时间格式统一使用[ISO8601](https://www.w3.org/TR/NOTE-datetime)时间格式（logback默认就是ISO8601，无需特殊配置）。
2. 应用日志需要用以下两个模块（任选其一）格式化成JSON格式：
  - https://github.com/logstash/logstash-logback-encoder （无需使用它的appender，只用encoder，打到文件里）
  - https://github.com/logstash/log4j-jsonevent-layout
3. 日志文件路径： 统一打到tomcat的logs目录下，可以使用`${catalina.home}/logs`来确定logs目录。
4. tomcat容器的日志目录要映射到宿主机上。
5. 日志文件命名规范： 按日期每天生成一个日志文件，文件名格式： `app.2016-05-13.log`


**如果收集其它格式的日志，请自己根据需要编写logstash配置文件**
