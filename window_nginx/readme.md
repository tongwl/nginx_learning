参考教程：
http://nginx.org/en/docs/windows.html

步骤:
1. 下载nginx包，直接解压即可使用

2. 启动nginx
 首先所有的操作都在nginx根目录(此目录下存在一个文件nginx.exe)。

 可以由以下两种方式**启动nginx**：
 
 * 命令 `start nginx` 启动    
 * 直接点击nginx.exe运行 (不推荐！！会使你的cmd窗口一直处于执行中，不能进行其他命令操作)

3. 停止/重启nginx
   `./nginx.exe -s stop`	//fast shutdown
   `./nginx.exe -s quit`	//graceful shutdown
   `./nginx.exe -s reload`	//changing configuration, starting new worker processes with a new configuration, graceful shutdown of old worker processes
   `./nginx.exe -s reopen`	//re-opening log files