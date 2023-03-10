### 跨域访问

### 跨域是什么？
> 跨域，指的是浏览器不能执行其他网站的脚本。它是由浏览器的同源策略造成的，是浏览器施加的安全限制。

所谓同源是指，域名，协议，端口均相同，不明白没关系，举个例子：

> `http://v1.demo.io/index.html` 调用 
`http://v1.demo.io/server.php` （非跨域）
`http://v2.demo.io/index.html` 调用 
`http://v2.demo.io/server.php`（子域名不同:v1/v2，跨域）


> `http://www.demo.io:8080/index.html` 调用 
`http://www.demo.io:8081/server.php` （端口不同:8080/8081，跨域）

> `http://www.demo.io/index.html` 调用 
`https://www.demo.io/server.php` （协议不同:http/https，跨域）

### 解决方法

```php
header('Access-Control-Allow-Origin:*');//允许所有来源访问
header('Access-Control-Allow-Method:POST,GET');//允许访问的方式
```
php接口文件顶部黏贴以上源代码即可
