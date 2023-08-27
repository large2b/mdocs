## HeidiSQL

### 什么是 HeidiSQL

> HeidiSQL is free software, and has the aim to be easy to learn. "Heidi" lets you see and edit data and structures from computers running one of the database systems MariaDB, MySQL, Microsoft SQL, PostgreSQL and SQLite. Invented in 2002 by Ansgar, HeidiSQL belongs to the most popular tools for MariaDB and MySQL worldwide.

简单来说 HS 是一款可视化数据库系统管理软件，让你可以查看和编辑数据库的数据和结构。



### 下载安装

1. 下载

   官方网址：[Download HeidiSQL](https://www.heidisql.com/download.php)

   <img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230820235832159.png" alt="image-20230820235832159" style="zoom:67%;" />

   根据自己的需要选择下载。

   

2. 安装

   把压缩包解压到 `D:\Software\HeidiSql_12.5` 目录下。双击 `heidisql.exe` 即可打开软件。

### 使用

1. 新建会话。
   点击左下角`新建` 新建一个会话，填写相应的信息，注意这里的`依赖库`根据情况来选择。

   <img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230821000650142.png" alt="image-20230821000650142" style="zoom:67%;" />

2. 成功进入会话

<img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230821000737273.png" alt="image-20230821000737273" style="zoom:67%;" />



3. 尝试来新建一个 database

   点击`查询`，输入一段 SQL 语句，使用快捷键 `F9` 执行。

   ``` sql
   CREATE DATABASE nodejs_mysql_demo
   ```

   执行成功后可以在下方控制台看到相应的信息。



​		按下 `F5` 刷新，就能看到新建的数据库出现在左侧啦。

