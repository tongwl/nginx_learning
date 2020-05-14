参考网址：https://www.jianshu.com/p/0c9ca8c1b49c
或则参考pdf: linux下如何离线安装nginx - 简书.pdf

注意事项：
1. 该教程有一处错误，有一个包下不存在./configure，需要运行./config。
2. nginx默认安装在/usr/local/nginx
3. nginx默认的相对路径是/usr/local/nginx/html
4. 我们将license前端dist文件夹放到/usr/local/nginx/html下，并重命名为license
5. 修改/usr/local/nginx/conf/nginx.conf文件，让项目指向license文件夹：
location / {
            root   html;
            index  index.html index.htm;
        }
修改为
location / {
            root   html/license;
            index  index.html index.htm;
        }

6. 启动nginx
在目录/usr/local/nginx/sbin下存在一个nginx命令，直接运行命令  ./nginx即可

7. 输入网址访问项目，如果访问不通，那么有可能是防火墙的问题，使用以下两句命令关闭访问墙（以nginx端口80为例子）
service firewalld stop
firewall-cmd --zone=public --add-port=80/tcp --permanent 
