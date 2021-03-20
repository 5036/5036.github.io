---
layout: post
title: 'PHP-Notes-320'
date: 2020-3-20 15:05:21 +0800
tags: PHP
author: WuYi
color: rgb(255,90,90)
cover: '../assets/php10.png'
subtitle: 'PHP'
---



####  **一、PHP系统函数**

| 函数               | 功能                                                         | 用法                                |
| ------------------ | ------------------------------------------------------------ | ----------------------------------- |
| var_dump()         | 打印变量结构信息，包括类型和值。数组将递归展开值             | **var_dump** ( `$arg1...`);         |
| echo()：是语法结构 | 输出一个或者多个字符串,可不用（），用单引号或者双引号括起来。变量直接输出， | **echo** $arg1,$arg2...;            |
| isset()            | 检测变量是否设置并且值不为null时返回ture，反之false          | isset（$args）                      |
| empty()            | 检测变量是否为空                                             | empty（$args）                      |
| exit()             | 输出一条信息同时退出当前版本                                 | exit('退出成功')                    |
| die()              | 输出一条信息同时停止代码向下执行                             | die（‘代码已停止’）                 |
| iconv()            | 字符集按照指定编码转换                                       | iconv(incharset,outcharset,$str)    |
| uniqid()           | 获取一个唯一id（无参数）或者获取一个带前缀、基于当前时间微秒数的唯一ID（看参数）。 | uniqid([前缀名]，[true])            |
| gettype()          | 获取数据类型                                                 | gettype($args)                      |
| settype()          | 把变量$arg设置为某数据类型                                   | settype($args,"[int][string]...")   |
| serialize()        | 把$arg序列化，即转换成文本保存或者传输，且不丢失其类型和结构 | serialize(mixed $arg)               |
| unserialize()      | 把$str反序列化，返回序列化之前的类型和格式信息               | unserialize($str)                   |
| getcwd()           | 获取当前运行脚本的目录                                       | getcwd（）                          |
| basename()         | 返回路径的中文部分                                           | basename($url)                      |
| preg_match()       | 用$string去匹配正则表达式，把匹配的结果用$res返回匹配1或者不匹配0 | preg_match($string,正则表达式,$res) |



#### **二、进制转换函数**

| 函数           | 功能                | 用法                                                   |
| -------------- | ------------------- | ------------------------------------------------------ |
| decbin()       | 十进制 ——> 二进制   | decbin($num)                                           |
| decoct()       | 十进制 ——> 八进制   | decoct($num)                                           |
| dechex()       | 十进制 ——> 十六进制 | dechex($num)                                           |
| bindec()       | 二进制 ——> 十进制   | bindec($num)                                           |
| octdec()       | 八进制 ——> 十进制   | octdec($num)                                           |
| hexdec()       | 十六进制 ——> 十进制 | hexdec($num)                                           |
| base_convert() | 任意进制转换        | base_convert(转换的数值，该数值的进制，要转换成的进制) |

各进制的英文：

二进制：binary 十进制：decimal

八进制：octect 十六进制：hexadecimal



#### **三、常量函数**

| 函数                    | 功能                                       | 用法                             |
| ----------------------- | ------------------------------------------ | -------------------------------- |
| define()                | 定义常量，第三个参数选择是否对大小写敏感。 | define(常量名，常量值，【true】) |
| defined（）             | 判断某常量是否存在                         | define（常量名）                 |
| get_defined_constants() | 获取预定义常量                             | get_defined_constant()           |



#### **四、判断函数**

| 函数         | 功能                         | 用法         |
| ------------ | ---------------------------- | ------------ |
| is_bool()    | 判断是否为布尔类型           | is_bool()    |
| is_int()     | 判断是否为整形               | is_int()     |
| is_string()  | 判断是否为字符串             | is_string()  |
| is_float()   | 判断是否为浮点型             | is_float()   |
| is_numeric() | 判断是否为数字或者数字字符串 | is_numeric() |
| is_null()    | 判断是否为空                 | is_null()    |
| is_array()   | 判断是否为数组               | is_array()   |
| is_dir()     | 判断是否为路径               | id_dir()     |



#### **五、字符串函数**

| 函数                     | 功能                                                         | 用法                                  |
| ------------------------ | ------------------------------------------------------------ | ------------------------------------- |
| strstr()为strchr()的别名 | 返回 `$str` 字符串从 $`needle` 第一次出现的位置开始到结尾的字符串。且区分大小写，不想区分大小写请用：stristr() | **strstr** ( $str , `$needle` )       |
| strpos()                 | 获取$str中$needle第一次出现的位置（下标），没有返回false     | strpos($str,$needle)                  |
| strrpos()                | 获取$str中$needle最后一次出现的位置（下标），没有返回false   | strrpos($str,$needle)                 |
| substr()                 | 截取字符串$str从$start位置到$length个的字符串                | substr($str,$start,$length)           |
| implode()                | 用,把数组连接成字符串                                        | implode(',',$arr)                     |
| explode()                | 用，把字符串分割成数组                                       | explode(',',$str)                     |
| str_split()              | 把字符串$str分割成数组，每单位长度为5                        | str_split($str,5)                     |
| str_replace()            | 把字符串$str中的a用b替换                                     | str_replace(a,b,$str)                 |
| strtolower()             | 字符串转换成小写的                                           | strtolower($str)                      |
| strtoupper()             | 字符串转换为大写                                             | strtoupper($str)                      |
| ucfirst()                | 把字符串$str第一个字符转换成大写                             | ucfirst($str)                         |
| unwords()                | 把字符串中$str每个单词转换成首字母大写                       | unwords($str)                         |
| trim()                   | 去除字符串两端的空白字符和其他字符                           | trim($str)                            |
| rtrim()                  | 去除字符串右侧的空白字符和其他字符                           | rtrim($str)                           |
| strlen()                 | 获取字符串长度                                               | strlen($str)                          |
| substr_count()           | 统计字符串$str中一个字符串$a出现的次数                       | substr_count($str,"$a")               |
| str_repeat()             | 重复输出$str,次数为$num                                      | str_repeat($str,$num)                 |
| strpad()                 | 在$str的左侧用0填充使其长度为$length                         | strpad($str,$length,"0",STR_PAD_LEFT) |
| strrev()                 | 翻转字符串顺序                                               | strrev($str)                          |
| rand()                   | 取m-n之间的随机整数                                          | rand（m，n）                          |
| mt_rand()                | 取m-n之间的随机整数,获取速度比mt_rand()快                    | mt_rand(m,n)                          |
| pow()                    | 取m的n次方                                                   | pow(m,n)                              |
| number_format()          | 以千位分隔符方式格式化一个数字                               | number_format($n)                     |



#### **六、数组函数**

| 函数                 | 作用                                                       | 用法                           |
| -------------------- | ---------------------------------------------------------- | ------------------------------ |
| unset()              | 销毁指定的变量                                             | unset($arr)/unset($arr[n])     |
| array_values()       | 获取数组中所有的值且重新建立数字下标                       | array_values($arr)             |
| array_keys()         | 获取数组中所有键值                                         | array_keys($arr)               |
| is_array()           | 判断是否为数组                                             | is_array($arr)                 |
| in_array()           | 判断数组$arr是否包含某个元素$str                           | in_array($str,$arr)            |
| count()              | 统计数组长度/统计多维数组长度                              | count($arr)/count($arr,1)      |
| range()              | 建立一个1-9的数组                                          | rang(1,9)、range(a-z)          |
| array_merge()        | 连接多个数组为一个数组                                     | array_merge($arr,$brr…)        |
| array_rand()         | 在数组中随机抽取n个单元，返回键值，成为新的数组            | array_rand($arr,n)             |
| shuffle()            | 打乱数组顺序                                               | shuffle($arr)                  |
| each()               | 返回数组中当前元素的 键／值对 并将数组指针自动向前移动一步 | each($arr)                     |
| list():语言结构      | 把数组中的值赋给一些变量                                   | list($a,$b,$c)=$arr            |
| array_unshift()      | 在数组开头插入一个或多个单元                               | array_unshift($arr,$v1,$v2...) |
| array_push()         | 在数组最后插入一个或多个单元                               | array_push($arr,$v1,$v2…)      |
| array_pop()          | 将数组的最后一个元素移除并返回                             | array_pop($arr)                |
| array_key_exist()    | 判断数组中是否存在键$k                                     | array_key_exist($k,$arr)       |
| array_search()       | 在数组中搜索给定的值$v，如果成功则返回相应的键名           | array_search($v,$arr)          |
| array_flip()         | 交换数组的键和值                                           | array_flip($arr)               |
| array_count_values() | 统计数组中所有值出现的次数                                 | array_count_values($arr)       |
| array_unique()       | 移除数组中重复的值                                         | array_unique($arr)             |
| sort()               | 将数组按照值的大小升序排列                                 | sort($arr)                     |
| asort()              | 将数组按照值的大小升序排列且保持索引关系                   | asort($arr)                    |
| rsort()              | 将数组按照值的大小降序排列，重排索引                       | rsort($arr)                    |
| arsort               | 将数组按照值的大小降序排列，保持索引                       | arsort($arr)                   |
| natsort()            | 自然排序(符合人们日常使用的习惯)                           | natsort($arr)                  |
| ksort()              | 将数组按照键的大小降序排列，保留键名到数据的关联           | ksort($arr)                    |
| krsort()             | 将数组按照键的大小降序排列，保留键名到数据的关联           | krsort($arr)                   |
| array_sum()          | 对数组中所有的值求和                                       | array_sum($arr)                |
| key()                | 获取数组中遍历指针的位置(键)                               | key($arr)                      |
| current()            | 获取指针所在位置的值                                       | current($arr)                  |
| next()               | 将数组中指针后移一个位置                                   | next($arr)                     |
| prev()               | 将数组中指针前移一个位置                                   | prev($arr)                     |
| reset()              | 重置数组中指针位置(指向第一个位置)                         | reset($arr)                    |
| end()                | 将数组中指针移到最后一个位置                               | end($arr)                      |



#### **七、时间函数**

| 函数        | 作用                                           | 用法                                 |
| ----------- | ---------------------------------------------- | ------------------------------------ |
| time()      | 获取当前时间戳                                 | time()                               |
| mktime()    | 获取指定时间的时间戳                           | mktime (小时, 分钟, 秒 ,月 ,日, 年 ) |
| date()      | 将时间$tmp指定格式输出                         | date('Y-m-d H:i:s',$tmp)             |
| strtotime() | 将任何英文文本的日期时间描述解析为 Unix 时间戳 | strtotime("now")                     |



#### **八、数据库函数**

| 函数                | 功能                                                         | 作用                            |
| ------------------- | ------------------------------------------------------------ | ------------------------------- |
| mysql_connect()     | 链接mysql数据库                                              | mysql_connect($host,$user,$pwd) |
| mysql_query()       | 发送一条 MySQL 语句                                          | mysql_query(sql语句)            |
| mysql_fetch_assoc() | 在结果集中取出一行数据组成关联数组并返回，并且继续移动内部数据指针 | mysql_fetch_assoc($result)      |
| mysql_fetch_array() | 在结果集中取出一行数据组成数组并返回，并且继续移动内部数据指针 | mysql_fetch_array($result,参数) |
| mysql_fetch_row()   | 在结果集中取出一行数据组成索引数组并返回，并且继续移动内部数据指针 | mysql_fetch_row($result)        |
| mysql_select_db()   | 选择数据库                                                   | mysql_select_db(数据库名)       |
| mysql_num_rows()    | 获取查询结果记录数                                           | mysql_num_rows(查询结果)        |



#### **九、文件操作函数**

| fopen()             | 打开文件或者URL                                      | fopen(“filename”,“mode”)             |
| ------------------- | ---------------------------------------------------- | ------------------------------------ |
| fwrite()            | 在文件中写入内容                                     | fwrite("filename","内容")            |
| fclose()            | 关闭文件或URL                                        | fclose("filename")                   |
| file_put_contents() | 一步写入内容                                         | file_put_contents("filename","内容") |
| file_get_contents() | 一步读取内容                                         | file_get_contents("filename","内容") |
| fread()             | 读取指定长度文件内容                                 | fread("filename",字节数)             |
| filesize()          | 获取文件内容长度（字节数）                           | filesize("filename")                 |
| fgets()             | 读取一行                                             | fgets($handle,length)                |
| file()              | 把整个文件读入一个数组中                             | file("filename")                     |
| copy()              | 拷贝文件，新文件名为"newfile"                        | copy("filename","newfile")           |
| unlink()            | 删除文件                                             | unlink($filename)                    |
| filectime()         | 获取文件创建时间                                     | filectime($filename)                 |
| fileatime()         | 获取文件上次访问时间                                 | fileatime($filename)                 |
| filemtime()         | 获取文件修改时间                                     | filemtime($filename)                 |
| feof()              | 判断指针是否到达文件末尾                             | feof($filename)                      |
| json_encode（）     | 把数据编译成JSON数据                                 | json_encode($a)                      |
| json_decode（）     | 把JSON数据反编码为PHP数据变量参数为true时，返回array | json_decode($j，[false]/true)        |



#### **十、目录操作函数**

| 函数          | 功能                         | 用法                             |
| ------------- | ---------------------------- | -------------------------------- |
| mkdir()       | 创建目录，有0777是否递归创建 | mkdir("/path/to/my/dir", 0777);  |
| rmdir()       | 删除目录                     | rmdir($DIR)                      |
| opendir()     | 打开目录句柄                 | opendir($dir)                    |
| readdir()     | 读取目录                     | readdir($dir)                    |
| closedir()    | 关闭目录                     | closedir($dir)                   |
| rewinddir()   | 重置目录资源                 | rewinddir($dir)                  |
| file_exists() | 判断文件/目录是否存在        | file_exists($filename/$dir)      |
| rename()      | 对文件/目录重命名            | rename($filename/$dir，$newname) |
| dirname()     | dirname($path)               | 返回路径中的目录部分             |
| basename（）  | 返回路径中的文件名部分       | basename($path)                  |
| pathinfo()    | 获取路径信息                 | pathinfo($path，[options])       |



#### **十一、类函数**

| 函数                 | 功能                                                         | 作用                            |
| -------------------- | ------------------------------------------------------------ | ------------------------------- |
| class_exists()       | 判断类是否存在                                               | class_exists($classname)        |
| interface_exists()   | 判断接口是否存在                                             | interface_exists($name)         |
| method_exists()      | 判断方法是否存在                                             | method_exists($name)            |
| property_exists()    | 判断属性是否存在                                             | property($name)                 |
| get_class()          | 获取类名称                                                   | get_class()                     |
| get_parent_class()   | 获取父类名称                                                 | get_parent_class()              |
| get_class_methods()  | 获取类中的方法                                               | get_class_methods()             |
| get_class_vars（）   | 返回由类的默认属性组成的数组                                 | get_class_vars（）              |
| get_declared_class() | 获取已定义的类的名称                                         | get_declared_class()            |
| __toString()         | 将对象当字符串对待时调用                                     | __toString()                    |
| __construct()        | New对象时自动调用                                            | __construct()                   |
| __destruct()         | 销毁对象时自动调用                                           | __destruct()                    |
| __clone()            | 克隆对象时自动调用                                           | __clone()                       |
| __invoke()           | 把对象当做函数调用时自动调用                                 | __invoke()                      |
| __set()              | 给不可访问的成员属性赋值时自动调用                           | __set()                         |
| __get()              | 读取不可读取的成员属性的值时自动调用                         | __get()                         |
| __isset()            | 对不可访问的成员属性使用isset()或者empty()时自动调用         | __isset()                       |
| __unset()            | 对不可访问的成员属性使用unset()时自动调                      | __unset()                       |
| class_alias()        | 为类创建一个别名                                             | class_alias(原类,类别名)        |
| get_object_vars()    | 返回一个包含object可用的已定义属性和值的关联数组             | get_object_vars()               |
| is_a()               | 如果对象属于该类或该类是此对象的父类则返回 TRUE              | is_a($obj,$classname)           |
| is_subclass_of()     | 如果对象 object 所属类是类 class_name 的子类，则返回 TRUE，否则返回 FALSE。 | is_subclass_of($obj,$classname) |