# cmd下使用的命令
## ulimit -c unlimited 设置打开保存崩溃程序的core文件
## coredumpctl list 文件名 筛选出该文件名的core文件
## coredumpctl 列出所有文件的core文件
## coredumpctl gdb 进程ID 使用gdb进入core文件
## g++ -g cpp文件名 -o 可执行文件名
# gdb模式下面的指令
## run r 运行程序
## next n 使程序向下走一行，不进入函数
## step s  使程序向下走一行，进入函数
## break b cpp文件名：行数 打断点
## continue c 运行程序直到下一个断点
## backtrace bt 查看函数调用栈
## print p 打印变量值 对于正在运行的程序可以打印右值并执行语句控制变量值的，coredump的尸体文件不行
## up 转移视角到上一个函数调用栈（位置是导致进入当前函数的语句）
## down 转移视角到下一个函数调用栈
## list 当前行 打印当前行的上下文
## layout src 弄一个框显示源码全文
## set logging on 在当前目录下创建一个txt文件，记录命令行的输出，不能跟layout src同时使用
## set logging off
## quit q 退出
## info locals 打印当前调用栈的所有局部变量及其值
## info args 打印进入当前栈是传入的参数及其值
## ctl+x 后按 a 从layout src切换到命令行