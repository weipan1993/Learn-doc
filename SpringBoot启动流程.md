# SpringBoot启动流程
SpringBoot启动流程分为两个阶段，SpringApplication初始化和运行。

### SpringApplication初始化
1. 确定应用运行环境，默认Servlet.
2. 通过Spring Spi机制文件配置加载相关属性设置。

### SpringApplication运行
1. SpringApplicationRunListeners 加载应用监听器
2. ConfigrableEnvironment 配置环境模块和监听：包括创建配置环境、加载属性配置文件和配置监听
   1. ConfigFileApplicationListener 加载Spring默认的相关属性配置文件(application.yml)
3. ConfigrableApplicationContext应用上下文创建
4. 应用上下文准备工作
5. SpringApplication#refreshContext 刷新应用上下文信息交于Spring完成
6. 执行后续应用执行器
