---
title: hexo常用插件一
abbrlink: 2a82
date: 2019-04-13 10:50:20
categories: hexo
tags:
  - hexo
---
> Failure is the fog through which we glimpse triumph.
> 失败是迷雾，穿过它，我们就可以瞥见光明。 ——《钢铁侠》
 
hexo中 image插件,abbrlink插件,admin插件使用教程

<!-- more -->

### hexo-asset-image图片处理插件
```
npm install hexo-asset-image --save 
```
_config.yml加入
```
post_asset_folder:这个选项设置为true
```
```
hexo new name
会同时在——posts 下生成name.md和name文件夹
图片放入name中
使用:![desc](name/image.jpg);
```
### hexo-abbrlink 短地址插件
短链接插件
```
npm install hexo-abbrlink --save
```
hexo-abbrlink插件配置 让地址尽量短小精悍
```
abbrlink:
  alg: crc16
  rep: hex

permalink: lucky/:abbrlink/
```
使用后image省略文件夹名字.
```
![desc](image.jpg)
```

### hexo-Admin编辑器
```
npm install --save hexo-admin
```
```
hexo s
```
然后打开 http://localhost:4000/admin/ 就可以看到管理页面。

#### 问题
```
npm WARN deprecated minimatch@2.0.10: Please update to minimatch 3.0.2 or higher to avoid a RegExp DoS issue
```
当你安装 hexo-admin，执行 npm install –save hexo-admin 时，可能会遇到上面的错误提示，是因为你缺少了一些依赖，执行下面的就好了。
```
npm install minimatch@"3.0.2"  
npm update -d
```

#### Admin-Deploy
- win
  1.根目录新建admin_script文件夹
  2.新建hexo-d.sh文件，内容如下
  ```
  hexo g && hexo d
  ```
  3.进入文件夹执行下面命令 把sh加入可执行权限
  ```
  chmod +x hexo-d.sh
  ```
  4.修改_config.yml 加入配置
  ```
  admin:
    username: myfavoritename 
    password_hash: be121740bf988b2225a313fa1f107ca1
    secret: a secret something
    deployCommand: ./admin_script/hexo-d.sh
  ```
#### 密码保护
  1.打开setting，点击Setup authentification here输入用户名，密 码，密钥，下面会自动生成配置文件，复制加在hexo根目录下的_config.yml中：

  ```
  admin:
  username: myfavoritename
  password_hash: be121740bf988b2225a313fa1f107ca1
  secret: a secret something
  ```
  2.重启hexo，就可以看到登录页面了