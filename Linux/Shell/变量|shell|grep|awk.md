### Shell 变量：
* 例如name=”yang”，需要注意几点，
    * 变量名需要符合正常编程语言的变量名要求；
    * 变量名，等号，值之间不能有空格；
    * 使用变量就是$name即可；
    * 双引号会对字符进行转义，单引号会进行忽略，全部都是字符串
    * 反斜杠用作转义字符
    * $()和``都是把里面的字符串当做命令执行，然后进行赋值
    * 如果是用英文符号进行判断，就必须用[中括号]，如果用大于小于这些，就必须用两个小括号才行。
    * 进行if判断时记得有头头尾，开始了if，就必须开始fi
### Grep 用法
  * 如果反向查找，把前面的输出作为后面的输入, 例如我想找出某一个进程但是不想看到我搜索的那个进程，如果搜索ps aux | grep “python”就会搜索出含有python名字的相关进程，如果想过滤掉含有grep的进程，就这样写ps aux | grep “python”| grep –v “grep”即可。
### Awk 用法
  * 例如我想在grep的写法上面获得PID，首先必须只能有待处理一行，否则会有多个数据被处理，然后在加 | awk ‘{print $2}’即可。
