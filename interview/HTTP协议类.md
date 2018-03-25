### HTTP协议的主要特点

- 简单快速
- 灵活
- 无连接



### 无状态HTTP报文的组成部分

请求报文（请求行、请求头、空行、请求体）

响应报文（状态行、响应头、空行、响应体）



### HTTP方法

- GET：获取资源
- POST：传输资源
- PUT：更新资源
- DELETE：删除资源
- HEAD：获得报文首部



### POST和GET的区别

- GET在浏览器回退时是无害的，而POST会再次提交请求
- GET产生的URL地址可以被收藏，而POST不能
- GET请求会被浏览器主动缓存，而POST不会，除非手动设置
- GET请求只能进行url编码，而POST支持多种编码方式
- GET请求参数会被完整保留在浏览器历史记录里，而POST中的参数不会被保留
- GET请求在URL中传送的参数是有长度限制的，而POST没有限制
- 对参数的数据类型，GET只接受ASCII字符，而POST没有限制
- GET比POST更不安全，因为参数直接暴露在URL上，所以不能用来传递敏感信息
- GET参数通过URL传递，POST放在Request body中



###  HTTP状态码

- 1xx：指示信息---表示请求已接收，继续处理
- 2xx：成功---表示请求已被成功接收
- 3xx:  重定向---要完成请求必须进行更进一步的操作
- 4xx：客户端错误---请求有语法错误或请求无法实现
- 5xx：服务器错误---服务器未能实现合法的请求




- 200 OK：客户端请求成功
- 206 Partial Content：客户端发送了一个带有Range头的GET请求，服务器完成了它
- 301 Moved Permanently：所请求的页面已经转移至新的url
- 302 Found：所请求的页面已经转移至新的url
- 304 Not Modified：客户端有缓冲的文档并发出了一个条件性的请求，服务器告诉客户端原来的缓冲文档还可以继续使用
-   400 Bad Request：客户端请求有语法错误，不能被服务器所理解
- 401 Unauthorized：请求未经授权，配合WWW-Authenticate报头域一起使用
- 403 Forbidden：对被请求页面的访问被禁止
- 404 Not Found：请求资源不存在
- 500 Internal Server Error：服务器发生不可预期的错误
- 503 Server Unavailable：请求未完成，服务器临时过载或宕机，一段时间后可能恢复正常



