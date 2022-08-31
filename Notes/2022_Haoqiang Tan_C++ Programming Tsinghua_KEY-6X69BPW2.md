# C++ Programming Tsinghua
## Metadata
- ItemType: book
- Authors: [[ Haoqiang Tan]]
- Collection: [[C++]]
- Date: 2022-08
- PDF Attachments: [C++程序设计第3版 (谭浩强) (z-lib.org).pdf](zotero://open-pdf/library/items/ECYG9VVR)
- Tags: #reading

👣➿👣

## VSCode & Obsidian
- Powershell and cmd
	- conda config --set auto_activate_base false
	- conda activate base; conda deactivate base
- Git update:
	- go to the directory of workspace
	- git add .
	- git commit -m "xxxx"
	- close the proxy
	- git push origin main

## 第四章-数组
- 一个数组，一种数据类型
- 数组的大小不能是变量，一定是一个固定的值，可以是int a[5]; 或者 const int n=5; int a[n];
- 一维数组只能逐个引用值，如a[0]=a[5]+a[7];
- 数组可以引用也可以赋值，如上例，二维数组是一样的
- 范围要注意：声明语句int a[3]\[4]; （数组三行四列）后面不能引用a[3]\[4] 没有这个元素；即前者表示维数或者说长度，后者代表下标值（从零开始）
- **数组名**作为函数**实参或形参**时传递的是数组的**起始地址**（首元素的地址），因此形参也可以是指针变量来存放地址
- 函数参数&数组：
	1. 数组元素为函数实参：此时只是把实参变量的值传给形参变量；形参变量修改，不影响实参变量/原数组
	2. 数组名为函数实参：引用时fun(a,5) // 5 is length，定义时void fun(int a[], int n)，即形参为数组名或者指针变量
		- 函数形参为数组名时，那么实参数组和形参数组共享一段内存；形参数组修改后，实参数组也被修改；然而形参变量和实参变量是不会的
		- 函数定义时，int a[] 只代表一维数组并接收首元素地址，并不分配内存单元，长度参数无意义
- 字符数组：
	- 字符串总是和字符数组联系起来，为了存放字符串必须定义字符数组
	- 字符串结束标志：'\0'（ASCII码为0的字符，空操作符，不显示，什么也不干） 通过它的位置确定字符串长度
	- 赋值三种：
		1. char c[5]={'I','a','m','Y','D'}; 初始化赋值
		2. char c[]="IamYD";  用字符串常量来初始化字符数组，其长度为6（系统自动加空字符）
		3. char c[5]; c[0]='I'; ... 即逐个赋值
	- 输入输出两种：
		1. int str[20]; cin>>str; cout<\<str; 用字符数组名str输入输出字符串，代表首元素的地址
		2. 逐个字符输入输出
	- 形参设定最好：void top_country(char country[]\[20], int n)  其中不指定第一维大小（即国家的个数n），设置一个形参n来表示个数
- 字符串类string 以及 字符串变量（对象）：
	- 基本类型包括：char、int、float、double
	- string是在标准库中声明的字符串类，以类定义对象
	- 好处：定义时不需要指定长度，不必担心overflow；可以赋值；可以通过index修改某个字符；cin和cout
	- 运算：不需要特定函数，和python一样；原因：基本运算符的重载
	- 字符串数组：字符串组成
	- char array，string，string array声明见code




👣➿👣