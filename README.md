# front-end

#### 正向代理与反向代理
正向代理是用户端部署/使用/代理，目的为了隐藏客户端，可用作翻墙  
反向代理是服务端部署/使用/代理，目的为了隐藏服务端，可用作负载均衡  
更形象地，正向代理: (客户端->代理服务器)->目标服务器，反向代理: 客户端->(代理服务器->目标服务器s)  
参考地址：https://www.zhihu.com/question/24723688

#### 同源策略和跨域问题
同源策略，它是由Netscape提出的一个著名的安全策略，所谓同源是指，域名，协议，端口相同  
一个域内的脚本仅仅具有本域内的权限，可以理解为本域脚本只能读写本域内的资源，而无法访问其它域的资源  
解决跨域的方法：  
前端方式：Jsonp(只支持GET);document.domain(一级域名相同);postMessage;Websocket;  
后端方式：跨来源资源共享CORS(Cross-Origin Resource Sharing);代理服务器(Proxy);  
参考地址：http://www.jianshu.com/p/fccabaf38ac2

### webpack
see my project react's webpack config  
参考地址：http://www.jianshu.com/p/dcb28b582318

### nginx
使用nginx处理静态文件资源，采用反向代理处理动态请求  
`  
location / {  
   root html;  
   index  index.html index.htm;  
}  
location /api {  
   proxy_pass   http://localhost:8080;  
}
 `
下载地址：http://nginx.org/en/download.html
