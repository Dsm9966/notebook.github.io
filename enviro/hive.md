## Hive

### 在命令行开始配置Hive,服务器具有hive压缩包
#### 1 tar -zxf apache-hive-1.2.1-bin.tar.gz
#### 2 mv apache-hive-1.2.1-bin hive
#### 3 cd hive/
#### 4 pwd ：/home/hadoop/hive
#### 5 vim /etc/profile:配置环境变量(同JAVA_HOME;HADOOP_HOME)
#### 6 . /etc/profile

   ![image.png](https://upload-images.jianshu.io/upload_images/14466577-f7084238c6d71a88.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#### 7 hive 

   ![image.png](https://upload-images.jianshu.io/upload_images/14466577-8c3b4c2cb04ef4f3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

####  
### 启动mysql基础上，在mysql内的操作：
####  mysql -u root -p(刚开始没有密码就登陆成功)
#### MySQL> UPDATE mysql.user SET Password=PASSWORD('新密码') where USER='root';
   #### 注意：新密码必须和下面操作中10步骤中密码相同
#### MySQL> flush privileges;
#### MySQL> mysql -u root -p(再次登录，输入密码登陆成功)
#### 设置mysql能够远程访问（放置mysql-connector-java-5.1.34.jar包）：
#### （1）mysql>GRANT ALL PRIVILEGES ON `*`.`*` TO 'root'@'%' IDENTIFIED BY 'youmysqlpassword' WITH GRANT OPTION;
#### （2）mysql>FLUSH PRIVILEGES
####  MySQL> exit   
#### 
#### 8 cd conf(pwd:/home/hadoop/hive/conf)
#### 9 touch hive-site.xml
#### 10 vim hive-site.xml

   ![image.png](https://upload-images.jianshu.io/upload_images/14466577-c2b9a8de43e1ac37.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
   
#### 11 hive 检查是否能正常进入
#### 运行Navicat 
    
  ![image.png](https://upload-images.jianshu.io/upload_images/14466577-253f8e5148f19364.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

  ![image.png](https://upload-images.jianshu.io/upload_images/14466577-82033c0e9af35d6d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)




