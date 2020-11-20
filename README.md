# man 命令
- 学习linux系统编程的时候，经常需要通过man手册查看某个函数的使用方式，例如查看它的参数
、返回值以及使用案例。而且，有时候我们不知道那个函数具体叫什么名字，只知道关键字大概
是什么，这时候可以使用man命令的`-k`选项
	+ `man -k keyword | grep "name"`
	+ 如: `man -k timer | grep "set"`

- 查找关键字为keyword的结构体、类型以及函数原型的定义, `typedef`可以替换为`define`尝试查找
	+ `grep "keyword" /usr/include/*.h | grep "typedef"`
	+ `grep "keyword" /usr/include/*/*.h | grep "typedef"`
	+ 如: `grep "time_t" /usr/include/*.h | grep "typedef"`
