# PortScanner
````

        ░█▀█░█▀█░█▀▄░▀█▀░█▀▀░█▀▀░█▀█░█▀█░█▀█░█▀▀░█▀▄
        ░█▀▀░█░█░█▀▄░░█░░▀▀█░█░░░█▀█░█░█░█░█░█▀▀░█▀▄
        ░▀░░░▀▀▀░▀░▀░░▀░░▀▀▀░▀▀▀░▀░▀░▀░▀░▀░▀░▀▀▀░▀░▀

        luogenji@hotmail.com(stathub.cn)     ver 1.0
````

PortScanner 是一款跨平台开放端口高性能审计小工具。它通过扫描`服务器`或`IP/IP段`的已知或未知开放端口，最终以审计清单向你报告情况。

### 特性功能：
```

跨平台支持,windows 7、windows 10、centos、ubuntu、mac os 及 arm
快速扫描，数秒完成上千个端口扫描
全自动更新常见、敏感、高危端口资源表
支持端口开放监测通知
可指定端口范围
可指定IP地址范围
将扫描结果保存到本地

```

### 软件截图
- 界面 1
![image.png](https://github.com/Heismart/portscanner/blob/main/help.png)

- 运行结果
![image.png](https://github.com/Heismart/portscanner/blob/main/scaned.png)

### 安装使用

根据操作系统，直接下载对应已编译好的运行文件即可。

https://github.com/heismart/PortScanner/tree/master/bin


### 帮助信息
````

        ░█▀█░█▀█░█▀▄░▀█▀░█▀▀░█▀▀░█▀█░█▀█░█▀█░█▀▀░█▀▄
        ░█▀▀░█░█░█▀▄░░█░░▀▀█░█░░░█▀█░█░█░█░█░█▀▀░█▀▄
        ░▀░░░▀▀▀░▀░▀░░▀░░▀▀▀░▀▀▀░▀░▀░▀░▀░▀░▀░▀▀▀░▀░▀

        luogenji@hotmail.com(stathub.cn)     ver 1.0



 Usage: PortScanner [-h 帮助] [-host ip地址或域名]  [-port 端口号范围] [-thread 并发] [-timeout 超时时长] [-log-dir 扫描日志保存路径]

CLI参数:

  -h    帮助信息
  -host string
        ip地址 例如:-ip=192.168.0.1-255 或 stathub.cn (default "127.0.0.1")
  -log-dir string
        日志地址 例如:-log-dir=ipaddr_scan.log (default "logs")
  -port string
        端口号范围 例如:-port=80,81,88-1000
  -skip-knowports
        默认拓展扫描系统收录的6000+已知端口. 设置为false可缩短扫描时间. (default true)
  -thread int
        并发总线程数 例如:-n=100 (default 100)
  -timeout int
        每端口超时时长(毫秒) 例如:-t=200 (default 200)
````

## 用例演示
#### Case 1：用 100 并发线程扫描特定主机名(或域名)上的特定端口号集，
```
PortScanner -port 80,81,88-3306 -host 163.com -thread 100
```
#### Case 2：扫描特定IP范围,如：192.168.8.1-255，80-1024的端口
```
PortScanner -host 192.168.0.1-255 -port 80-1024 -thread 100
```

##### ！扫描结果存放在logs目录中，以当前[host]_scaned.[时间戳].log命名，该目录可通过-log-dir指定路径

## 后续计划

[ ] 端口服务审计，识别端口实际对应的应用服务

[ ] 端口服务弱口令及安全审计,如：Mysql,Mongodb,Redis等

[ ] 服务化支持端口开放审计及安全审计通知



