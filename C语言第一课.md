# C语言第一课

## VS的下载与安装

## VS的创建项目相关问题

1. **打开别人的文件，点击.sln文件**
2. 窗口布局
   	* 没有解决方案的窗口：在视图中找
   	* 基本的视图：解决方案管理、类视、输出、错误列表、工具箱
3. 设置字体
   	* 工具--选项--环境--字体与颜色  控制台字体-15号
   	* 工具--文本编辑器--c/c++--行号
4. 编译运行程序
   	* 不太聪明的方法是在调试窗口。快捷键：Ctrl+F5
5. 怎么去找生成的exe
6. 同一个解决方案添加多个方案
   	* 设置为启动项
7. 改字符集：右键项目，项目属性，常规，使用Unicode的字符

## 一些常见的错误

1. LINK : fatal error LNK1561: 必须定义入口点

   没有写入口函数或者入口函数没写对，入口函数默认为main函数，可以更改，但是没必要。

## C语言程序

1. 最简单的程序：

   ~~~c
   int main()
   {
       return 0;
   }
   ~~~

   其它形态：

   ~~~c
   void main()
   {
       
   }
   
   void main(void)
   {
       
   }
   void main()
   {
       return;
   }
   ~~~

   **注意：不要把main写成mian**

2. c语言中的注释

   >单行： //
   >
   >多行：/**/
   >
   >25%的注释量

3. c语言的头文件：

   1. 库文件：别人写的

      > include  目录下的所有的.h文件，用尖括号的方法去包含，右键打开，然后打开文件目录。#include <stdio.h>
      >
      > #include "stdio.h" ,""包含.h文件
      >
      > #include  "D:\\myhead.h"   绝对路径
      >
      > **注意：c语言中的单斜杠（\）必须要用双斜杠(\\)或者（/）**
   
4. c语言基本的输出函数---printf()

   ~~~c
   #include <stdio.h>
   int main()
   {
       printf("hello world!");
       getchar(); //第一种防闪屏的方法
       getch();  //需要#include <conio.h>
       system("pause");  //需要#include <stdlib.h>
       //while(1); 不推荐
       return 0;
   }
   ~~~

   * 转义字符 \和特殊的字符组成

     * \n  换行

     * \t   制表符

       > 原理：每个数据按照8位制表
       >
       > 超过8位，按照16去制表

     * \a  响铃声

     * \r  --->光标移到行首，覆盖原来的。

5. system()函数

   * system("字符串"),将字符串反馈给操作系统(os)

   * system函数的功能

     * 执行dos命令  cls---清屏  pause---暂停

     * 运行应用程序   calc---计算器   mspaint---画图版

     * 调整格式

       color f0

       DATE/T

       TIME/T

     * 运行脚本文件  vbs文件    批处理文件(.bat)

   