highPerformanceNetworkApp
=========================
This project is not sourcecode, it is a way to design high performance network application from my 7 years experience in a big network company. <br>


This is my desktop in Shanghai Office, And I give the way step by step, you can try <br><br>
 ![image](https://raw.githubusercontent.com/wuqunfei/highPerformanceNetworkApp/master/myDesk.jpg)<br><br>
Thinking in high perfermance network application<br>
 ![image](https://raw.githubusercontent.com/wuqunfei/highPerformanceNetworkApp/master/logic.png)<br><br>
 
1. Choose a framework, it always depends on which kind system already exists and which kind hardware you can buy. For example, our ftp server is built by Python and rebuilt python code into C code to run, because we don’t have enough memory on each machine if we use JVM and don’t have enough time to develop by C++.<br>

2. Don’t repeat yourself, so we like use open source library also. Then we can add our logic into it. Open is free, but it will be many bugs and instability in many library. I always write email to contributor on discuss. It is inevitable and sometime it is terrible to add our own logic. Now I like to use some high active and stabile version to expand and add our business logic. In fact, writing our business into logic is faster then combination many framework and lib.<br>

3. Almost application is network, sometime we find our logic and code is perfect. But we still have bottleneck. Network will be the killer.  As my telecomm background, we always use Wireshark http://www.wireshark.org/ which is a packet analyzer. It is used for network troubleshooting, analysis, software and communications protocol development. It would be a great helper when you lost in trouble. <br>
![image](https://raw.githubusercontent.com/wuqunfei/highPerformanceNetworkApp/master/capture.png)<br>

4. Performance needs clients. But at first, we don’t have enough clients. So we always use HP LoadRunner which is an automated performance and test automation product from Hewlett-Packard for application load testing: examining system behaviour and performance, while generating actual load. I can write many kind test-script like Http,Ftp,Mysql on LoadRunner. Also it has perfect reports of your test and it has RPS/ TPS data on test-line. I think it is necessary tools to expend performance.<br>
![image](https://raw.githubusercontent.com/wuqunfei/highPerformanceNetworkApp/master/loadRunner.png)<br>
Image is from my open-source http://code.google.com/p/feitp-server/. It means the ftp server finished 1939 (TPS) Transaction Per Second. 1 upload ftp transaction needs about 5 times TCP/IP connection like Login, send pwd, open port, send file,bye, etc.<br>

5. Monitor performance is the feedback of your application. Sometimes we write some monitor script by ourselves. But nagios http://en.wikipedia.org/wiki/Nagios is more powerful than we can do. We use it in almost monitor projects in shanghai Network. Also we start to use zabbix framework to finish our monitor job, because it can monitor everything http://www.zabbix.com/monitor_everything.php and easy to second develop to customize our needs in python.<br>
![image](https://raw.githubusercontent.com/wuqunfei/highPerformanceNetworkApp/master/map.png)<br><br>

At last, I introduce something about myself. I am an IT engineer in Shanghai at Aclatel-Lucent Group China. More information at LinkedIn: http://de.linkedin.com/in/wuqunfei, Contact me: wu.qunfei@gmail.com Have a fun!
