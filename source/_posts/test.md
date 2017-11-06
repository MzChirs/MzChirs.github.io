---
title: AngularJs 报错信息
---

---
### 错误信息：遍历的数组中包含相同的项，则会抛错
data: 17-10-24 上午


``` bash
$ [ngRepeat:dupes] 
	http://errors.angularjs.org/1.5.8/ngRepeat/dupes?p0=s%20in%20bannerData&p1=string%3An&p2=n
```
##### 解决方法：
* 在对应的ng-repeat指令中增加track by $index

---
### 错误信息：
data: 17-10-24 上午


``` bash
$ [ng:areq]
	 http://errors.angularjs.org/1.5.8/ng/areq?p0=myCtrl&p1=not%20a%20function%2C%20got%20string
```
##### 解决方法：
* 有使用到$scope，就必须要用js代码来定义angularJS自定义控制器，也就必须要给ng-app进行赋值和初始化，否则就是会报这个错误。看到楼主的修正，我想到了我之前解决问题的步骤。我这里就是有在HTML中用到angularJS控制器却缺少了对ng-controller的定义。

---
### 错误信息：注入错误
data: 17-10-24 上午


``` bash
$ [$injector:unpr] 
	http://errors.angularjs.org/1.5.8/$injector/unpr?p0=marketServiceProvider%20%3C-%20marketService%20%3C-%20marketController
```
##### 解决方法：
* 暂时还没有具体的解决方法,具体来说就是代码哪里写错了，找找错误看看哪里有没有多写一个逗号或者少写一个逗号之类的。
自己少了一个逗号引起的。