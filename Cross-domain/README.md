### 跨域访问

### 跨域是什么？

 跨域，指的是浏览器不能执行其他网站的脚本。它是由浏览器的同源策略造成的，是浏览器施加的安全限制。


### 解决方法

```php
header('Access-Control-Allow-Origin:*');//允许所有来源访问
header('Access-Control-Allow-Method:POST,GET');//允许访问的方式
```
php接口文件顶部黏贴以上源代码即可
