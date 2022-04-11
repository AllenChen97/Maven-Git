# [Maven](https://www.bilibili.com/video/BV1dp4y1Q7Hf)

## 1. 简介

### 1.1. Why maven - 让开发人员专注于开发
相对于传统的项目开发：
1. Maven可以管理模块和模块之间的关联关系
2. 项目需要用很多第三方功能，自动导入各类jar包
3. jar包的版本管理
4. 管理jar包之间的依赖

另外：
- maven还会编译项目和测试
- 打包项目成jar/war
- 部署项目

### 1.2. 项目构建 - 生命周期 - 常用命令 (重要)
1. 清理 clean: 把编译好的清理掉
2. 编译 compile: 一次性编译所有java-class文件，javac是一个一个编译的
3. 测试 test: 可批量测试和丰富的测试功能
4. 报告 report: 生成测试报告
5. 打包 package: 把代码打包成jar/war包，作为项目的结果文件
6. 安装 install: 把jar包安装到本机仓库
7. 部署 deploy: 让安装好的程序可以执行

## 2. 核心

### 2.1. 核心概念
1. pom: 对象模型，可以控制maven构建的过程，管理Jar和依赖
2. 坐标:唯一字符串，标识资源
3. 插件和目标: 执行maven构建的时候用的工具就是插件


### 2.2. 安装
1. 下载解压
2. 环境变量: M2_HOME=maven目录 和 path=%M2_HOME%\bin
3. 测试 mvn -v

### 2.3. maven编译
- 首次使用要下载很多插件在 c:\Users\Allen\.m2\repository 
- 如果要修改默认仓库位置：/conf/settings.xml 的 <localRepository>

仓库调用顺序：
1. 本地仓库
2. 私服
3. 镜像
4. 中央仓库

### 2.4. pom文件
- modelVersion: maven版本，对于maven2和3来说，该值只能是4.0.0  

坐标：标识项目
- groupId: com.公司.业务/项目
- artifactId: 模块名/项目名
- version: 迭代版本，带-snapshot 快照表明项目还在开发还不是稳定的  

其他：
- packaging: 打包拓展名，默认是jar，也可以改成war, pom, rar, ear等
- dependencies 依赖
- properties 设置属性
- build maven项目构建时的配置信息
- parent

### 2.5. Junit测试
- public void testAdd(){}
- public void是必须的，命名建议 test+方法名
