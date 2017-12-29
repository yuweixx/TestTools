## 数据库安装:
### 一、安装服务器：
1.启动安装程序后，填一下邮箱;
2.下一步到关键步骤；
3.关键步骤a，设置字符集为```Unicode(AL32UTF8)```;
4.关键步骤b，设置管理员默认密码;
5.下一步直到安装完整;
6.安装完成后在Net Configuration Assistant中，配置监听服务，选择tcp协议，端口1521即可。

### 二、安装客户端：
1.启动安装程序，选择runtime即可;
2.安装路径要记好，后续要检查环境变量和登录器配置。

### 三、登录器安装：
1.启动安装程序，选择下一步即可;
2.安装完成后，要确认Tools-Preferences-Connection中OCI library的配置正确的指向客户端的安装路径。

### 简体中文编码环境变量配置:
``` NLS_LANG=SIMPLIFIED CHINESE_CHINA.ZHS16GBK ```

## 常用操作
### 备份数据库:
``` exp username/password file=D:\db_back\dbfilename.dmp log=D:\db_back\logfilename.log ```

### 登录:
``` sqlplus / as sysdba; ```

### 删除用户及数据:
``` drop user username cascade; ```

### 关闭数据库:
``` shutdown abort; ```

### 开启数据库:
``` startup; ```

### 创建新用户:
``` create user newusername identified by newpassword; ```

### 给新用户授权:

``` grant connect,resource,create any view to newusername; ```
``` alter user newusername quota unlimited on users; ```

### 还原数据库数据:
``` imp "'/ as sysdba'" file=D:\dbback\dbfilename.dmp fromuser=newusername touser=newusername buffer=819200 ```

