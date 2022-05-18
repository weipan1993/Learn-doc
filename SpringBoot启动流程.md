# SpringBoot启动流程
SpringBoot启动流程分为两个阶段，SpringApplication构建和运行。

### SpringApplication构建
1. 确定应用运行环境，默认Servlet.
2. 通过Spring Spi机制文件配置加载相关属性设置。

### SpringApplication运行
1. 加载应用监听器
2. 准备环境相关信息
   a. 加载Spring默认的相关属性配置文件
