## 清华日报

学生健康和出行情况报告每日自动提交

强烈建议使用第二种方式，简单易行.


### 正常使用方式

* pip install -r requirements.txt
* 配置 conf.ini 输入清华info 用户名与密码
* python report.py
* 创建定时任务 Windows/Linux


### 非正常使用方式
> 如果你没有服务器，或者自己电脑也不能保证时刻开启，
那么Github Action可以作为你的服务器自动定时执行,并且非常安全。
>
* fork该仓库到你的项目，下面都是设置你的项目
* 进入: Settings-> Secrets-> 添加USER_NAME与USER_PASS两个key, 对应value为你清华info的用户名与密码 // **Important!**
![添加Secrets](https://github.com/naihaishy/TsinghuaDailyReport/blob/master/results/c.png)
* 进入: Actions 点击 Understand  // **Important!**
![Understand](https://github.com/naihaishy/TsinghuaDailyReport/blob/master/results/d.png)
* 编辑: .github/workflows/deploy.yml 随便修改点什么,例如修改时间或者加个注释，然后commit // **Important!**

**OK !**

**说明**
> 1.一定要修改deploy.xml然后commit, 系统会检测到Actions，然后加入到定时任务中，否则不会触发定时
> 
> 2.Github Actions的配置文件(.github/workflows/deploy.yml)中配置了时间 
默认是每天北京时间10:00 可以自行修改
>
> 3.Github Action服务器时间为UTC格式,比北京晚8个小时;
> 除此之外，它要慢几分钟(5分钟左右), 自己测试时多等待5分钟左右
> 
> 4.运行日志去 Action下面查看



### 效果图
![效果图1](https://github.com/naihaishy/TsinghuaDailyReport/blob/master/results/a.png) 
![效果图2](https://github.com/naihaishy/TsinghuaDailyReport/blob/master/results/b.png) 
![效果图3](https://github.com/naihaishy/TsinghuaDailyReport/blob/master/results/e.png) 
![效果图4](https://github.com/naihaishy/TsinghuaDailyReport/blob/master/results/f.png) 
