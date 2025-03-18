# paste-web
此文件内容放至htdocs文件夹（或子文件夹）下即可食用，加强安全性请继续阅读
访问请前往http(s)://localhost/(子文件夹名）

# 预览：
![屏幕截图-2025-03-08-190753](https://zhouzhou12203.github.io/picx-images-hosting/屏幕截图-2025-03-08-190753.8vn2amf6pj.webp)
# 修改密码请分别修改delete.php、hide.php、pin.php中的密码，默认密码是12203

# 防止访问其余文件请在.htaccess文件里添加如下内容：
注意.htaccess文件是使用apache2搭建网站的结果，
```
# 阻止直接访问 data.json
<FilesMatch "12203data.json">
    Order Allow,Deny
    Deny from all
</FilesMatch>

# 阻止直接访问.js文件
<FilesMatch "(core|helper|api)\.js$">
    Require all denied
</FilesMatch>

# 允许访问 proxy.php
<Files "proxy.php">
    Order Allow,Deny
    Allow from all
</Files>
```
