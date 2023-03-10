### 防止反向代理

### 原理

> 使用php一段代码实现防止反向代理

### 应用场景

- 新开站点遭反代导致搜索引擎对其域名降权
- 排名竞争遭反代导致搜索引擎对其域名降权

### 源代码

```php

<?php 
/**
 * 防止反向代理
 * author: Tom
 * links: https://www.docsget.com
 * GitHub: https://github.com/mytom1998
 **/
if($_SERVER['SERVER_NAME'] != 'docsget.com' ||$_SERVER['SERVER_NAME'] != 'docsget.com' )
{
exit('非法反向代理访问');
}
?>

```

### 注意事项

请将源代码内的域名`docsget.com`替换，否则运行代码直接返回 `非法反向代理访问`。

如果本身建立的页面为`.html`更改为`.php`
