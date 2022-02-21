1. 查看当前的ubuntu是否安装了ssh-server服务。默认只安装ssh-client服务
>```dpkg -l | grep ssh```
2. 安装ssh-server服务
>```sudo apt-get install openssh-server```
3. 确认ssh-server是否启动,如果看到sshd那说明ssh-server已经启动了
>```ps -e | grep ssh```
4. 启动
>```sudo /etc/init.d/ssh start```  
```sudo service ssh start```
5. 配置相关：
>ssh-server配置文件位于/etc/ssh/sshd_config，在这里可以定义SSH的服务端口，默认端口是22，你可以自己定义成其他端口号，如222  
然后重启SSH服务：  
```sudo /etc/init.d/ssh stop```  
```sudo /etc/init.d/ssh start```
6. 查看服务器ip
>```ifconfig```