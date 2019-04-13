---
title: 正则表达式
abbrlink: 9f6b
date: 2019-04-13 17:03:14
tags: regExp
categories: regExp
---

有时间每天巩固一下薄弱的知识=>正则表达式
<!-- more -->
## 1. 创建 RegExp 对象语法
```
let reg = new RegExp("pattern","attributes");
```
### 1.1 五大属性
   属性|描述
   -|-
   globla |RegExp 对象是否具有 g标志 全局匹配
   ignoreCase|RegExp 对象是否具有 i标志 大小写敏感
   lastIndex| 一个整数, 表示开始下一次匹配的字符位置
   multiline| RegExp 对象是否具有 m标志 多行匹配
   source | RegExp 对象的源文本  
### 1.2 RegExp 对象的方法
  方法|描述
  -|-
  exec|检索字符串中指定值，返回值，并确定其位置
  test|检索字符串中指定值，返回true or false
  
  ```
  var reg  = new RegExp(/\d/,'g');
  var str = "1e2r3t4";
  var r = ''
  while(r!=null){
     r = reg.exec(str)
     console.log(r)
  }
  // 全局匹配 所以需要循环多次 直到 r=null结束

  console.log(reg.test(str)) // true
  
  ```
  Array[0] 就是value 
  Array[index] 匹配位置
  Array[input] 源文本
  ![exec](9f6b/regexp1.png)
