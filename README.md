# MIPS-Single-Cycle-Processor

Ryan的注释

* 安装icarus iverilog（verilog编译器），下载地址http://bleyer.org/icarus/iverilog-v11-20210204-x64_setup.exe
* 安装DVKit（Verilog编辑器），http://dvkit.sourceforge.net/

打开windows命令行，运行
```
verilog -o main -s mips_testbench -c command.txt
```
其中
`-o`表示输出的可执行文件名
`-s`表示root module（如果是需要运行测试，则应使用`mips_testbench`)
`-c`包含所有输入的`*.v`文件

然后运行
```
vvp main
```
此命令会生成`res_data.mem`和`res_register.mem`两个文件。这些文件记录了registers运行时的变化。

测试请参考参考`ALU_testbench.v`的写法。

未解决问题：
1. 如何把assembly编译成二进制代码放到`code.txt`里？可以用Mars来做吗？
2. Mars还有其他用处没有？
3. `code.txt`里面到底写什么？
