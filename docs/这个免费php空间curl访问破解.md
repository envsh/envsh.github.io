---
JoplinID: 2KGSh61Z3ED5WLja7INiTb
NostrID: 
来源: 
tags:
  - tagaa
  - tagbb
  - mkdocs
  - shitnet
  - api
  - php
  - web
创建: 2024-03-14 11:23
更新: 2024-03-24 14:18
---
这个免费php空间curl访问破解

curl -H 'cookie: __test=2100f677379726e88cad0937c094c1f6'  'http://fixlan.free.nf/pif.php?aa=hhh&i=2' -A 'firefox'

只需要带一个cookie就可以了
这个cookie是最初请求的js生成的，是一种challenge机制。
生成算法还没有仔细看，想获取这个cookie，从浏览器访问一下就可以。
只是不知道这个cookie有效期多久，如果频繁失效，还是挺麻烦的。

ftp上传文件太差了，还不如直接搞PHP上传。就是上传目录有麻烦。
这个空间的流量好像不大，也没法安装PHP版的http代理服务器。
好像还有PHP超时限制。超时60秒还好。
好像还没有https支持。可以安装免费证书，三个月有效期。而提供的免费证书，在现在的浏览器都是红色警告的。
不给保存访问日志，需要自己写日志文件。
是否支持执行命令行?

5 GB Disk Space
Unlimited Bandwidth
Unlimited Hosted Domains
MySQL database 5G
PHP最大内存 512M
最大POST 32M

做代理好像可以，无限流量。
服务器不支持connect方法。。。

```
* CONNECT tunnel: HTTP/1.1 negotiated allocate connect buffer
* Establish HTTP proxy tunnel to google.com:443                                        > CONNECT google.com:443 HTTP/1.1
> Host: google.com:443
> User-Agent: curl/8.6.0
> Proxy-Connection: Keep-Alive               > * TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
* TLSv1.3 (IN), TLS handshake, Newsession Ticket (4):
< HTTP/1.1 400 Bad Request                    < Server: nginx
< Date: Thu, 14 Mar 2024 05:19:58 GMT
< Content-Type: text/html
< Content-Length: 150
< Connection: close

 ```

嗨难用难搞

可以再本地再开一个标准代理APP，转换一下上游http代理需要cookie的问题，这样就解决了。
因为要处理额外的非标准流程，需要自己编写或者修改代理程序。

```
function toNumbers(d){var e=[];d.replace(/(..)/g,function(d){e.push(parseInt(d,16))});return e}function toHex(){for(var d=[],d=1==arguments.length&&arguments[0].constructor==Array?arguments[0]:arguments,e="",f=0;f<d.length;f++)e+=(16>d[f]?"0":"")+d[f].toString(16);return e.toLowerCase()}var a=toNumbers("f655ba9d09a112d4968c63579db590b4"),b=toNumbers("98344c2eee86c3994890592585b49f80"),c=toNumbers("5388e947470e84923bd9824b8b24fd3c");document.cookie="__test="+toHex(slowAES.decrypt(c,2,a,b))+"; expires=Thu, 31-Dec-37 23:55:55 GMT; path=/"; location.href="https://fixlan.free.nf/index.php?i=1";


```

生成的cookie超过十年，应该不用搞他的算法，需要的时候浏览器生成一个就可以了。



更新：2024-03-24 14:18 字数：1874/2616
