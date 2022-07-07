# 使用VSC 开发STM32的程序

1. 环境的搭建  
vscode(需要关于arm的插件)  
stm32cubemx  
mingw-w64  
arm-none-edbi-gcc  
openocd
2. vscode的配置  
查看配置代码，配置了头文件地址，define，windows相关  
仿真相关 openocd  
vscode debug相关


## makefile笔记:  
  $@--目标文件，$^--所有的依赖文件，$<--第一个依赖文件。  

make会在当前目录下找名字叫“Makefile”或“makefile”的文件。  

-E 预处理	把.h .c展开生成一个 .i  
-S 汇编：   .i生成一个汇编代码文件  .s    
-c 编译：	.s生成一个 .o .obj   
-o 链接：	.o链接生成一个 .exe  .elf   
 --- 
 第一个文件是目标文件
.PHONY:  
伪目标  
= （替换） += （最佳）  ：= （恒等于 常量）  
本质是将 arm-gcc 命令生成文件，链接到一起，生成一个新文件
$(变量名)  替换  
通配符 $^所有的依赖文件 $@所有的目标文件  $< 所有的依赖文件的第一个文件
