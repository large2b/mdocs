## MySQL

### 安装

1. 下载

   MySQL官网：[Download MySQL Community Server](https://dev.mysql.com/downloads/mysql/)

   选择适合的版本，这里选择 `5.7.43 64bit` 版本。

   <img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230820194812434.png" alt="image-20230820194812434" style="zoom: 67%;" />

​		

​	下载完成后，解压到 `D:\Software\mysql-5.7.43-winx64` 下  

2. 配置环境变量
   选择` 高级系统设置 -> 环境变量 -> 系统变量`

   1. 点击新建，新建一个名为 `MYSQL_HOME`的系统变量，变量值是你安装 MySQL 的路径，点击确定。

      <img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230820213315741.png" alt="image-20230820213315741" style="zoom:67%;" />

   2. 点击系统变量下的 PATH 变量，新增一条`%MYSQL_HOME%\bin`

      <img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230820213459729.png" alt="image-20230820213459729" style="zoom:67%;" />

3. 配置 mysql
   如果`mysql-5.7.43-winx64` 目录下没有 `my.ini`文件，手动新建一个，把下面的内容复制进去。

   其中 `basedir`  和  `datadir ` 要换成自己的目录路径

   ``` 
   [mysqld]
   
   # 设置3306端口
   
   port=3306
   
   # 设置mysql的安装目录
   
   basedir=D:\Software\mysql-5.7.43-winx64
   
   # 设置mysql数据库的数据的存放目录
   
   datadir=D:\Software\mysql-5.7.43-winx64\data
   
   # 允许最大连接数
   
   max_connections=200
   
   # 允许连接失败的次数。这是为了防止有人从该主机试图攻击数据库系统
   
   max_connect_errors=10
   
   # 服务端使用的字符集默认为UTF8
   
   character-set-server=utf8
   
   # 创建新表时将使用的默认存储引擎
   
   default-storage-engine=INNODB
   
   # 默认使用“mysql_native_password”插件认证
   
   default_authentication_plugin=mysql_native_password
   
   [mysql]
   
   # 设置mysql客户端默认字符集
   
   default-character-set=utf8
   
   [client]
   
   # 设置mysql客户端连接服务端时默认使用的端口
   
   port=3306
   
   default-character-set=utf8
   ```

   

4. 正式安装 mysql
   以管理员身份打开命令行工具，运行下面的命令 

   ```bash
   # 1
   mysqld -install
   
   # 2
   mysql --initialize
   ```

5. 开启 mysql 服务

   ``` bash
   net start mysql # 开启
   net stop mysql # 关闭
   ```

6. 输入指令进入 mysql 服务

   ``` bash
   mysql -u root -p
   ```

   这里会要求你输入密码，临时密码储存在 `D:\Software\mysql-5.7.43-winx64\data` 目录下以`.err` 结尾的文件中

   <img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230820224621183.png" alt="image-20230820224621183" style="zoom:67%;" />

7. 修改密码

   初次进入需要更改密码。

   ``` bash
   ALTER USER 'root'@'localhost' IDENTIFIED BY 'new password';
   ```



至此，已经成功安装 MySQL 啦。