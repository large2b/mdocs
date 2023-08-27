## NVM

nvm 是 nodejs 的版本管理工具，能够实现同时安装多个版本的 node 并 丝滑切换。



*** 注意，安装 nvm 之前，如果已经安装了 node，需要把 node 完全卸载***



### 下载安装

1. 下载
   官方地址：[[Releases · coreybutler/nvm-windows (github.com)](https://github.com/coreybutler/nvm-windows/releases)](https://nvm.uihtm.com/)

   <img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230821002428467.png" alt="image-20230821002428467" style="zoom:67%;" />

   

2. 安装

   - 选择 nvm 路径
     `D:\nvm`

   - 选择nodejs 路径

     `C:\Program Files\nodejs`

     

3. 安装完成确认

   打开命令行工具，输入

   ``` bash
   nvm
   ```

   如果打印出  nvm 的提示信息，说明安装成功。



### 简单的使用 nvm

#### 使用阿里云镜像

下载之前最好切换镜像源，不然下载会很慢

```bash
nvm npm_mirror https://npmmirror.com/mirrors/npm/
nvm node_mirror https://npmmirror.com/mirrors/node/
```



#### 安装 nodejs

1. 查看可用版本

   ```bash
   nvm list available
   ```

   <img src="C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230821003504687.png" alt="image-20230821003504687" style="zoom: 80%;" />

2. 选择版本并安装

   例如：安装 18.17.1

   ```bash
   nvm install 18.17.1
   ```

   或者

   ```bash
   nvm install @18
   ```

   这样会获取 node 18 的最新版本



#### 查看已安装 node 版本

```bash
nvm list
```

nvm 管理的所有 node 版本和 当前使用的 node 版本将会被展示：

![image-20230821004247907](C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230821004247907.png)

#### 切换 node 版本

打开命令行工具，输入

```bash
nvm use 你想要使用的 node 版本
```



验证一下 node 版本是否使用成功

```bash
node -v
```

打印出 node 版本号说明成功。

![image-20230821005429194](C:\Users\large2b\AppData\Roaming\Typora\typora-user-images\image-20230821005429194.png)

