#从 URL 输入到页面展现
###URL是什么？
统一资源定位符。用于定位互联网上的资源。
URL中又包括：
1. 协议方案名：http, https, ftp, file 等。 以 http://www.jirengu.com/app/watch/1327/1?vsum=3&fastVer=1 举例。 该URL用的是http协议
2. 服务器：如 www.jirengu.com
3. 端口号：一般默认不设置为80
4. 路径：/app/watch/1327/1
5. 询问：?vsum=3&fastVer=1

###域名解析流程
1. 浏览器缓存 – 浏览器会缓存DNS记录一段时间
2. 系统缓存 - 从 Hosts 文件查找是否有该域名和对应 IP
3. 路由器缓存 – 一般路由器也会缓存域名信息。
4. ISP DNS 缓存 – 比如到电信的 DNS 上查找缓存。
5. 如果都没有找到，则向根域名服务器查找域名对应 IP，根域名服务器把请求转发到下一级，直到找到 IP
 -  电脑上不了网，为什么修改dns为8.8.8.8 或者114.114.114.114?
8.8.8.8是Google公司的DNS服务器。当本地ISP都没有办法找到该域名的对应IP的时候，可以尝试用Google提供的DNS服务器查找域名。国内114.114.114.114是另一个提供DNS服务的服务器。
 -  dns 劫持是什么？
DNS劫持就是通过劫持了DNS服务器，通过某些手段取得某域名的解析记录控制权，进而修改此域名的解析结果，导致对该域名的访问由原IP地址转入到修改后的指定IP，其结果就是对特定的网址不能访问或访问的是假网址，从而实现窃取资料或者破坏原有正常服务的目的。

###Web服务器
- 常见的 web服务器有 Apache、Nginx、IIS、Lighttpd
- web服务器接收用户的Request 交给网站代码，或者接受请求反向代理到其他 web服务器

![Paste_Image.png](http://upload-images.jianshu.io/upload_images/2491597-7eb0d5bd5bd8d67a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###网站处理流程
 - #####MVC 模型(model)-视图(view)-控制器(controller)
![](http://upload-images.jianshu.io/upload_images/2491597-af4a4d73727cd8ba.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

###浏览器处理
1. HTML字符串被浏览器接受后被一句句读取解析
2. 解析到link 标签后重新发送请求获取css
3. 解析到 script标签后发送请求获取 js，并执行代码
4. 解析到img 标签后发送请求获取图片资源

###绘制网页
浏览器根据 HTML 和 CSS 计算得到渲染树，绘制到屏幕上js 会被执行