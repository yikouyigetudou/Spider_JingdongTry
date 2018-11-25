# Spider_JingdongTry
用python爬虫模拟浏览器来自动申请京东试用。<br>
注意：此程序仅作为学习爬虫练习使用，不得扩散出去另作他用。<br>

### README 目录
* [依赖](#依赖)
* [Method_First](#Method_First)
  * [使用说明](#使用说明)
  * [功能特点](#功能特点)
* [Method_Second](#Method_Second)
  * [使用说明](#使用说明-1)
  * [功能特点](#功能特点-1)
  * [待实现的功能](#待实现的功能)
* [参考资料](#参考资料)

### 依赖
* Python 3.6
* ChromeDriver([官网地址](https://sites.google.com/a/chromium.org/chromedriver/))
* selenium 3.14.1
* pyquery 1.4

## Method_First
作者：[Jonariguez](https://github.com/Jonariguez)

* 已经申请过的商品就不会再申请了
* 申请的时候采用**headless模式**进行，就不用浏览器界面了，无限接近**无扰模式**
* 程序开始运行时会打开Chrome浏览器并打开[京东官网](https://www.jd.com),只需要在该浏览器登录即可，之后浏览器会关闭，此时便开始申请商品。

### 使用说明
1. 直接运行Try_selenium.py文件即可
2. 程序开始会自动打开浏览器，手动登录账号
3. 等浏览器关闭之后，程序开始申请试用

### 功能特点
- [x] 采用headless模式，无浏览器界面
- [x] 分离自定义设置文件config
- [x] 指定申请商品个数或者页数
- [x] 自定义用户登录所用时间
- [x] 是否申请完成后自动关机


## Method_Second
作者：[jzplp](https://github.com/jzplp)

### 使用说明
1. 鼠标点击mian.py文件即可执行
2. 待浏览器打开京东官网后，手动登陆京东账户。
3. 等待若干秒后，程序自动执行，不需要人工操作。
4. 程序运行可能需要一小时左右。期间不能关闭模拟的浏览器。

### 功能特点
* 代码是在Method_First的之前代码上改动的。
* 商品过滤
  * 控制商品售价，低于某个数值便不申请
  * 实现了简单的关键字过滤功能，出现某些关键字便不申请
* 限制每天申请商品的个数，超过便不申请
* 可以控制申请商品的类别
* 申请完成后自动在log.txt中记录申请的时间和申请数量

### 待实现的功能
- [ ] 优化程序结构
- [x] 在商品列表处剔除已经申请过的商品
- [ ] 自动检测登陆成功并5秒后开始试用
- [ ] 登陆成功后自动关闭浏览器，用headless模式试用
- [ ] 断点续申
  - [ ] 记录申请过的类别和页数，当天第二次打开时从此处开始继续
  - [ ] 记录申请过的商品数，当天第二次打开时继续计数
- [ ] 申请完成可以自动关闭电脑
- [ ] 添加图形界面


## 参考资料
* Python3网络爬虫开发实战  <br>
  https://germey.gitbooks.io/python3webspider/content/
* xmlns属性导致pyquery查询元素失败 <br>
  https://blog.csdn.net/zx1245773445/article/details/82821642
