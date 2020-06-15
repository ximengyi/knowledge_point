##### 1 requeire与 include

require则会导致一个致命性错误且脚本停止执行
include在引入不存文件时产生一个警告且脚本还会继续执行
    

##### 2 get post

GET 和 POST 方法没有实质区别，只是报文格式不同
GET 和 POST 只是 HTTP 协议中两种请求方式，而 HTTP 协议是基于 TCP/IP 的应用层协议，无论 GET 还是 POST，用的都是同一个传输层协议，所以在传输上，没有区别
GET 方法的参数应该放在 url 中，POST 方法参数应该放在 body 中
get 和post 都是不安全的，都可以完整的截获报文



4 array_merge array+
array_merge相同的字符串键名后者会替代前者，相同的数字键名，后者不会替代前者，而是数字会重新排序
array+ 连个数组中存在相同的键名时，后者不会取代前者，而是忽略后者

5 echo print print_r
echo 是语句 print 是函数有返回值,print_r可以打印数组和对象


6 跨域问题
1使用ajax或者jquery的jsonp方式
2 服务器hearder头设置Access-Control-Allow-Origin
3nginx 反向代理
7redis 和memache
1Redis不仅仅支持简单的k/v类型的数据，同时还提供list，set，hash等数据结构的存储
2灾难恢复，memcache挂掉后，数据不可恢复，redis挂掉后可以通过aof恢复
3数据存储安全，memcache挂掉，数据不可恢复，redis可以定期写到磁盘持久化

8session 和cookie
1、cookie数据存放在客户的浏览器上，session数据放在服务器上。
2单个cookie保存的数据不能超过4K，session可以存储
3cookie在客户端容易被窃取，数据保存在session里更加安全

9
$_SERVER['REMOTE_ADDR']
$_SERVER['SERRVER_ADDR']
$ip = $_SERVER['HTTP_X_FORWARDED_FOR'];



tcp 三次握手四次挥手
9 string 常用函数

1.  strpos 查找字符串
$pos = strpos($mystring, $findme);
if ($pos === false) {
}else{
}
2   

<?php
$rest = substr("abcdef", 0, -1);  // 返回 "abcde"
$rest = substr("abcdef", 2, -1);  // 返回 "cde"
$rest = substr("abcdef", 4, -4);  // 返回 ""
$rest = substr("abcdef", -3, -1); // 返回 "de"
?>

3 mb_strstr ( string $haystack , string $needle [, bool $before_needle = false [, string $encoding = mb_internal_encoding() ]] )  
4 mb_split ( string $pattern , string $string [, int $limit = -1 ] ) : array mb_split — 使用正则表达式分割多字节字符串
5  
$str = 'abcdafd123f.exe';
$str = mb_split('\.',$str);
$name = $str[0];
echo $name;

6

implode ( string $glue , array $pieces ) : string 将一维数组转化为字符串

7设置定时脚本

10 redis 问题
https://www.cnblogs.com/jasontec/p/9699242.html

11 mongodb 问题
12 mysql 问题

