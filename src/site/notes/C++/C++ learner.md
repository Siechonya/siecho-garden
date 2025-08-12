---
{"dg-publish":true,"permalink":"/C++/C++ learner/","noteIcon":"","created":"2024-10-27T18:33:52.711+08:00","updated":"2025-08-07T16:44:44.422+08:00"}
---



# CH.1 pre.

## 1. procedures of compiling

​	editor：edit code

​	compiler：翻译为机器语言 $\rightarrow$ object code（.o）

​	linking：link with lib && your code $\rightarrow$ 可执行代码

```c++
cin.get(); // 读取下一次键击，防止.exe“一闪而过”
```



# CH.2 start to learn C++

​	<font color="#ff0000">C++对大小写敏感</font>

## 1. function definition && function prototype（函数原型）

```c++
//an example of function prototype
double pow(double, double);
//an example of function definition
type function_name(arguments_type, arguments){
    statements;
    return xxx;
}
```

​	函数定义不能嵌套；

## 2. iostream: standard input && output stream header(标准输入输出流库)

```c++
// if
using namepace std; //使用命名空间(少用, 以免冲突)
// then
cout << ... << endl; && cin >> variable; //(不推荐)
// else:
std::cout << ... << std::endl; && std::cin >> variable; //(推荐)

//attention:
cin >> s1 >> s2;
// ">>" can be interrupted by (space), 空格符被视为cin输入流的分割点
// means that if you input "hello world!", then s1="hello", and s2="world!"
```

## 4. 关键字

## 5. pre-processor directives (预处理器命令)

### 5.1 header file && linking (头文件和链接)

```c++
//Declaration && Definition
//必须在变量和函数的定义之前声明，注意不同文件的定义可能冲突，两种方案：
extern int num;	//num在其他文件定义,且不是static(局部变量)
#include "header"	//num在头文件中定义
//同一文件中的同一作用域中，变量不能声明两次, 而const可以重复定义
```

### 5.2. Macro(宏)

```c++
#define PI 3.14	//声明常量自变量
//相比于const，这只是一种文本替换，在此用途下是不安全的

//支持参数的宏定义
#define max(a, b) (a > b ? a : b)

//当然，因为是文本替换，甚至可以用其“定义”函数而不“声明”：
#define print_pointer_of_num \
				int *ptr = &number; \
				cout << ptr <<endl;
int number = 10;
print_pointer_of_num;

//也可以做传递参数的版本：
#define print_pointer_of_num(num) \
				int *ptr = &num; \
				cout << ptr <<endl;
int number = 10;
print_pointer_of_num(number);
```

### 5.3. 条件编译

```c++
//#if ... #endif 条件编译段可以框住代码段：
#if 0
#include "header.h"
#define PI  3.14
int a = 1;
#endif 	/// 中间三行代码相当于被注释了，但只需修改为 #if 1　就可以解除注释

//判断是否已经有相关的宏定义
#ifndef PI
#define PI 3.14
#endif
//等同于：
#if !defined(PI)
#define PI 3.14
#endif

//#elif #else也是可用的，记得结尾的 #endif
```





# CH.3 simple figure type && operation (简单数据类型和操作符)

## 1. basic variables

variables name // 变量名命名规则采取标识符规则, 即 :

- 包含字母, 数字, 下划线
- 不能以数字开头

### 1.1 basic variables
基本变量类型主要包括(s.d. 表示 significant digits（有效位数）) :

| 整型(bit)        | 符号前缀     | 字符&小整数    | 布尔类型 | 浮点数(bit&s.d.)       | 自动   |
| :------------- | :------- | :-------- | :--- | :------------------ | ---- |
| short(16)      | signed   | char      | bool | float(32&6)         | auto |
| int(32)        | unsigned | wchar_t   |      | double(64)          |      |
| long(>32)      |          | char16_t  |      | long double(80~128) |      |
| long long(>64) |          | char_32_t |      |                     |      |
> addition:
> 单独的 unsigned 指 unsigned int
> cin 和 cout 将输入和输出视作 char stream，对于 wchar_t stream 应当用 wcin 和 wcout

### 1.2 sizeof && typedef
```c++
sizeof(类型名 or 变量名);	//内置函数sizeof()返回字节数(bytes)
typedef typename newname;	//typedef, 定义变量的别名
```


### 1.3 const(常量)限定符

```c++
//supposed to initialize when declaring(建议在声明的同时进行初始化)，ex：
const int toes = value;
```

## 2. operators(操作符)

| type操作符类型      | 符号                                  |
| -------------- | ----------------------------------- |
| 运算             | +, -, *, /, %                       |
| 关系             | ==, !=, >, <, >=, <=                |
| 逻辑             | &&, \|\|, !                         |
| 位运算            | 略                                   |
| 自增自减           | ++, --                              |
| 运算赋值           | =, +=, -=, /=, *=, %=               |
| 位操作赋值          | 略                                   |
| 条件操作           | ?=                                  |
| 逗号（返回最右端操作数的值） | <expression_1>, <expression_2>, ... |

```c++
// ?= 条件操作符的运用
<expression> ? <when expression True> : <when expression False>;
//the result of <expression> is bool (表达式的值是布尔类型)
//可以嵌套
```

操作符优先级: 略(建议适当多使用括号)

```c++
// attention：int/int = int, 解决方式:
std::cout.setf(ios_base::fixed, ios_base::floatfield); // fixed-point,阻止科学计数法表示
```

## 3. type conversion
### 3.1 implicit（隐式转换）

$$
\begin{array}c
bool\rightarrow char\rightarrow unsigned\ char\rightarrow\ short(wchar\_t)\rightarrow\ unsigned short(wchar\_t)\rightarrow int\rightarrow unsigned\ int
\\\rightarrow long\ int\rightarrow unsigned\ long\ int\rightarrow float\rightarrow double\rightarrow long\ double
\end{array}
$$
```c++
//in general，转换方向是：低精度->高精度，短字节->长字节，signed->unsigned
//while, there's some special case:
//(1)右值转换成左值的类型, 比如float运算赋值给int变量
//(2)条件操作符 ||　条件语句　将<expression>转换成bool：0->False
```

### 3.2 forced/explicit（强制/显式转换）

```c++
// ex.
typename(variable);	//C-style
(typename)variable;
//attention: 上述操作仅在表达式中暂时利用转换后的类型

int_object = static_cast<int>(float_object);	//C++-style, 将float对象转为int并赋值给新的int对象

//其他强制转换类型的函数: const_cast, dynamic_cast, reinterpret_cast
```

## 4. 注释与换行

```c++
//双斜线表示单行注释

/*
成对或多行注释使用 /* ... */
*/

//用 "\" 对代码进行换行:
xxxxxxxxxxxxxxxx \
    xxxxxxxxxxxxxxxxxxx;
```

# CH.4 statement(语句)
## 1. simple statement
```c++
//空语句(NULL)
;
```

## 2. complex statement(复合语句)
### 2.1 条件语句
#### if
```c++
//if
if(<expression>){
    //when <expression>'s True
    xxxxxxx;
} else if(<semi-expression>){	//when <expression>'s False
    //when <semi-expression>'s True
    xxxxxxx;
}
//.........
else{
    //when all of the expreesions' False
    xxxxxx;
}
```
#### switch
```c++
//switch:适合枚举
switch(object){
    case 0:	//if object==0
        xxxxxxx;
        break;	//否则，将依次执行后面case下的语句xxxxxxx;（无视case条件），称为"fall-through"
    case 1:
        xxxxxxx;
        break;
    //......
    default:
        xxxxxxxx;
        break;
}
```

### 2.2_循环语句
#### while
```c++
//while
while(<expression>){
    xxxxxxxx;	//if <expression> is True
}
```
#### do...while
```c++
//do...while
do{
    xxxxxx;	//if <expression> is True
}while(<expression>);
```
#### for
```c++
//for
for(int i=0; i<10; i++){
    xxxx;
}
```

### 2.3 跳转语句
```c++
//break：jump out of one loop body

//continue：end this loop in advance，start to next loop straightly

//goto
label:
	xxxxxxxx;
if(<expression>){
    goto label;
}
```

# CH.5 (Complex) 复合数据类型
## 1. array (数组: 静态数据结构)
```c++
typename arrayName[arraySize];	//declaration
//attention: arraySize is necessary, which isn't a variable
char week[7];	//create array of 7 short, the last index is std::strlen(week) - 1
week[0] = 'm';	//assign value
int iarray[3] = {1, 2, 3};	//initializing
int iarray[3]{1, 2, 3};	//initializing, okay with c++11
int iarray[3] = {1, 2};	//initializing, non-assigned elements' going to be set to 0
int iarray[3] = {};	//initializing, all elements will be set to 0
char week[7] = "mtwsfss";	//initializing
int inarray[] = {2, 3, 4};	//initializing without arraySize, initialization is necessary
int num_elements = sizeof inarray / sizeof(int);	//the number of elements

// !not allowed operations
inarray = iarray;	//copy, but arrayName's not a left-value, so it's wrong
iarray = {3, 2, 1};	//assign all value instead of initializing
```
## 2. C-style string
C 语言中的字符串

` '' refer to char(ASCII), while "" refer to str`

$\color{blue}{C-style\ string\ need\ header:\ \langle cstring\rangle}$

```c++
#include<cstring>
char str1[5] = {'0', '1', '2', '3', '\0'};	//a string must with '\0' at th end, otherwise called char array
char str2[5] = "0123";	//the same, and the '\0' is understood
char str3[] = "0123";	//let the compiler count
//attention: as counting the arraySize, '\0' inclued
"123""456";	//str concatenation

char str4[] = "0123";
std::strlen(str4)	//return 4, char num before \0 (it's not arraySize)
```
## 3. vector (向量: 数组的替代, 动态数据结构)
$\color{blue}{vector\ need\ header:\ \langle vector\rangle}$
```c++
//initializing ex.
#include<vector>
vector<int> vec0; //only declare, vec0 is null
vector<int> vec00(3); //declare a int vector with length of 3, it's elements are default initial value
vector<int> vec1(3, 100); //declare a int vector with length of 3, all of it's elements are 100

//some operations
vector<int> vec2(vec1);	//copy vec1 to vec2, 深拷贝deep copy
vec1.size();	//similar to string.length()
vec1.empty();	//return True when vec1's empty
vec1.push_back(99);	//similar to list.append(99) in python
vec1.pop_back();	//remove an element from the end
cout << vec[1] << endl;	//access elements by index
```
## 4. C++ style string
可以视为 $vector \langle char\rangle$

$\color{blue}{C++\ style\ string\ need \ header:\ \langle string\rangle}$
```c++
//initializing ex.
#include<string>
string s1(3, 'a');
string s2("s2's value");
string s3(s2);	//copy

//we can apply string, same as vector<char>

s1 = s1 + s2;	//concatenate
```
## 5. struct (结构体)  

## 6. class (类)

# CH.6 (Derived) 派生数据类型
## 1. pointer(指针)
```c++
//definition ex.
int *ptr1;	//unsafe declaration
int *ptr = NULL; //safe declaration, null pointer, its value is 0(or said 0x00000000).
int arr[5]={0};	int *ptr2 = arr; //safe declaration
int num = 0;  int *ptr = &num;
//! After definition, ptr means &num (address), while *ptr means num (value which is pionted to). At this moment, * is called "dereference operator"(解引用运算符).

typename *type1_ptr, *type2_ptr; //right
int* ptr1, ptr2; //prt1 is a pointer, while ptr2 is int

void *ptr; //a pointer, but we don't kown type that it points to. Usually uesd in certain function which handles systemic memory.

// basic operation 基本操作
int num = 0;
int *ptr = &num;
&num; //Get address取地址 ==ptr
*ptr; //dereference解引用 ==num

// arithmetical operation 算术操作
int array[5] = {0, 1, 2, 3, 4};
int *ptr = array;
*(ptr + 2); // == *(array + 2) == array[2] == 2
*(ptr - 2); //unsafe, program may crash
int *ptr1 = array + 1;
ptr1 - ptr; // == 1, Pointer subtraction 指针相减
ptr - ptr1; // == -1

//const pointer常指针
const int num = 3;
// int *ptr1 = &num, 错误, 普通指针不能指向const变量, 正确的定义方式:
const int *ptr2 = &num;
// const 指针可以指向普通变量:
int num0 = 4;
ptr2 = &num0;
// *ptr2 = 4 , 错误, const指针不能修改解引用后的值, 但可以修改指向的地址:
const int num1 = 5;
ptr2 = &num2;
```

