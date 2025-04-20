# paste-web
此文件内容放至htdocs文件夹（或子文件夹）下即可食用，加强安全性请继续阅读
访问请前往http(s)://localhost/(子文件夹名）

参考：http://zhou12203.top/2025/03/04/网络剪贴板简易搭建/
# 预览：
![屏幕截图-2025-03-08-190753](https://zhouzhou12203.github.io/picx-images-hosting/屏幕截图-2025-03-08-190753.8vn2amf6pj.webp)
# 修改密码请分别修改delete.php、hide.php、pin.php中的密码，默认密码是12203
# 功能
- 4月更新：新增markdown语法显示和换行效果
1. 在保存和删除功能基础上，增加删除、置顶、隐藏、安全代理、提交频率限制功能；
2. 隐藏状态下复制内容均为“此内容已被隐藏”；
3. 增加data.json记录ip功能；
4. 优化移动端显示；
5. 修复了可以直接访问data.json的数据安全问题，增加安全代理；注意，需在.htaccess文件中添加以下内容，此方法针对Apache搭建网站方式；
6. 修复了F12/检查元素能够看到隐藏内容的bug
# 部分缺陷
1. 未设置分页
2. 在F12查看原文件情况下刷新页面会出现data.json中储存的数据，但是通过过滤文件实现了隐藏内容不显示、记录ip不显示的功能
# 防止访问其余文件请在.htaccess文件里添加如下内容：
注意.htaccess文件是使用apache2搭建网站的结果，
# 建议
1. 修改页面背景颜色可直接修改index.html的<style>部分
2. 提交频率可在RateLimiter.php中修改频率
```
# 阻止直接访问 data.json
<FilesMatch "12203data.json">
    Order Allow,Deny
    Deny from all
</FilesMatch>

# 允许访问 proxy.php
<Files "proxy.php">
    Order Allow,Deny
    Allow from all
</Files>
```
