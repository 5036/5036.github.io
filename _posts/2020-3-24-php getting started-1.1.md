---
layout: post
title: 'PHP-Notes-324'
date: 2020-3-24 13:05:21 +0800
tags: PHP
author: WuYi
color: rgb(255,210,32)
cover: '../assets/php11.png'
subtitle: 'PHP'
---



#### NOTE

#### `empty()`可以向括号中间传入一个变量。这个变量的值如果为false或者为null的话，返回true

{% highlight ruby %}
<?php
$apple = null;
$result = empty($apple);
var_dump($result);
?>
{% endhighlight %}

#### `isset()`可以向括号中间传入一个或者多个变量，变量与变量间用逗号分开。只要有有一个变量为null，则返回false。否则，则返回true

{% highlight ruby %}
<?php
$one = 10;
$two = false;
$three = 0;
$four = null;
$result = isset($one , $two , $three , $four);
var_dump($result);
?>
{% endhighlight %}

#### `unset()`这个函数的功能是毁掉变量。unset(变量)括号中间插入想要毁掉的变量名，这个变量就会被毁掉。
{% highlight ruby %}
<?php
$one = 10;
unset($one);
var_dump($one);
?>
{% endhighlight %}

#### 使用`is_*` 系列函数。 `is_types`这一系列的函数，来进行判断某个东西是不是某个类型。如果是这个类型返回真，不是这个类型返回假。

**is_int 是否为整型   
is_bool 是否为布尔   
is_float 是否是浮点   
is_string 是否是字符串   
is_array 是否是数组   
is_object 是否是对象   
is_null 是否为空   
is_resource 是否为资源   
is_scalar 是否为标量   
is_numeric 是否为数值类型   
is_callable 是否为函数**

#### 下面的情况是布尔值判断时的自动类型转换:

**1，整型的0为假，其他整型值全为真   
2, 浮点的0.0，布尔值的假。小数点后只要有一个非零的数值即为真   
3，空字符串为假，只要里面有一个空格都算真   
4，字符串的0，也将其看作是假。其他的都为真   
5，空数组也将其视为假，只要里面有一个值，就为真   
6，空也为假   
7, 未声明成功的资源也为假**

#### 对象是一个复合类型

对象的英文叫`object，var_dump`一个变量的时候看到的类型为`object`的，这个变量就是对象类型
所谓复合类型：就是在一个类型中可以同时存入字符串、浮点、整型、布尔等

#### `define`(常量名，常量值)

**1.常量值只能为上一章中我们讲到的标量   
2.常量名可以小写，但是通常大写   
3.常量名可以不加引号，但是通常加上引号   
4.在字符串中调用常量的时候，必须在引号外面   
5.常量名建议只用字母和下划线**

|常量名|说明|
|-|-|
LINE|当前所在的行
FILE|当前文件在服务器的路径
FUNCTIOIN|当前函数名
CLASS|当前类名
METHOD|当前成员方法名
PHP_OS	PHP|运行的操作系统
PHP_VERSION|当前PHP的版本
TRAIT|Trait的名字,php5.4新加
DIR|文件所在的目录
NAMESPACE|当前命名空间的名称（区分大小写）

#### 常见词汇

include   
读音：[ɪnˈklud]   
解释：包含   

version   
读音：[ˈvɜ:ʃn]   
解释：版本   

user   
读音：[ˈjuzɚ]   
解释：用户   
复数：users   

define   
读音：[dɪˈfaɪn]   
解释：规定   
