#### 问题描述：
使用uniapp开发时，用到 new Date("2020-05-11 14:00:00").getTime(),在浏览器端显示一切正常，但在手机客户端显示为NaN

#### 原因说明：

有的手机系统不支持2019-04-29这样格式而支持2019/04/29这样的格式导致的

#### 解决方法：

```JavaScript
let createTime = "2020-05-11 14:00:00";
createTime = createTime.replace(/-/g, "/");
let timeStr = (new Date(createTime)).getTime();
```
