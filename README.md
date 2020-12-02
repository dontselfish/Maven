# Maven的安装步骤

## （一）下载安装包与安装JDK

- Maven官网链接：http://maven.apache.org/

![图1-1](note/1.PNG)

![图1-2](note/2.PNG)

- jdk7下载链接：https://repo.huaweicloud.com/java/jdk/7u80-b15/

    Maven需要jdk7低版本才能避免报错

![图1-6](note/6.PNG)

## （二）开始安装

### 1. 新建maven_work文件夹(可任意命名)
### 2. 解压安装包(apache-maven-3.6.3)到maven_work文件夹下

![图2-3](note/3.PNG)

### 3. 配置环境变量
    
新增系统变量
    
    <变量名>>MAVEN_HOME
    <变量值>>*\apache-maven-3.6.3
    
    <变量名>>CLASSPATH
    <变量值>>.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;

    <变量名>>JAVA_HOME
    <变量值>>C:\Program Files\Java\jdk1.7.0_80

    *号代表maven安装包文件夹所在的文件路径

![图2-4](note/4.PNG)

![图2-5](note/5.PNG)

![图2-7](note/7.PNG)

![图2-8](note/8.PNG)

配置系统变量Path

    <变量名>>Path
    <变量值>>在开头新增下列几个变量
        %JAVA_HOME%\bin;
        %JAVA_HOME%\jre\bin;
        %MAVEN_HOME%\bin;

![图2-9](note/9.PNG)

## （三）新建Hello项目

### 1. 项目约定的目录结构：
    <项目主目录>
    - Hello(文件夹)
    <项目Hello目录>
    - src(文件夹)
    - pom.xml(文件必须要有且要配置)
    <项目Hello>src目录>
    - main(文件夹)
    - test(文件夹)
    <项目Hello>src>main目录>
    - java(主程序java文件文件夹)
    - resources(配置文件文件夹)
    <项目Hello>src>test目录>
    - java(测试主程序java文件的文件夹)
    - resources(测试使用的配置文件文件夹)

项目结构树状图：

![图3-10](note/10.PNG)

### 2. 新建与配置<pom.xml>文件

配置如下所示：
    
    <?xml version="1.0" encoding="UTF-8"?>

    <project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    <groupId>com.dontselfish</groupId>
    <artifactId>ch01-maven</artifactId>
    <version>1.0-SNAPSHOT</version>
    </project>

之后保存即可。

### 3. 新建java类

