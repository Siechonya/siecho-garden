---
{"dg-publish":true,"permalink":"/C++/2_Cpp面向对象编程/","noteIcon":"","created":"2025-08-24T23:01:59.987+08:00","updated":"2025-08-26T23:44:34.405+08:00"}
---

# 1 类和继承  
## 1.1 类的概念  
### 1.1.1 结构体(Struct, C)  
用 `.` 访问结构体的成员.
```C++
#include <iostream>
#include <string>
#include <vector>
using namespace std;
// 借助结构体进行数据抽象
struct Student{
    int ID;
    int classNum;
    string name;
};

int main() {
    vector<Student> students;  // 声明一个向量students, 元素类型是结构体Student
    Student stu1;  // 声明结构体对象stu1
    stu1.ID = 5;  // 用点号访问结构体中的成员
    stu1.classNum = 1;
    stu1.name = "大宝";
    students.push_back(stu1);  // 将stu1添加到students数组
    Student stu2;  // 类似上面
    stu2.ID = 6;
    stu2.classNum = 1;
    stu2.name = "小宝";
    students.push_back(stu2);
    for ( int i = 0; i < 2; i++ ) {
        cout << "该学生的学号是：" << students[i].ID << endl;
        cout << "该学生的班级是：" << students[i].classNum << endl;
        cout << "该学生的名字是：" << students[i].name << endl;
        cout << endl;
    }
    return 0;
}
-----------------------------------------------------------
输出:
该学生的学号是：5
该学生的班级是：1
该学生的名字是：大宝

该学生的学号是：6
该学生的班级是：1
该学生的名字是：小宝
```  
### 1.1.2 封装  
封装: 隐藏细节, 将一个复杂的装置封装在一个黑匣子, 只提供一些用户接口. 如, 在使用函数时, 只需要关注参数类型 && 返回值 && 函数的作用, 而不需要关系函数体内具体的代码.  

类(Class)是 C++在 C 的结构体之上进行扩展的新类型, 可以同 Struct 一般实现数据抽象, 也可以使用访问控制符有效地体现封装. 比如, 上面的 `vector.push_back(...);`, 就是 vector 类的使用, 我们可以使用它的 `push_back()` 和 `pop_back()` 等函数, 而不必关心 vector 是如何实现的.  
### 1.1.3 继承和多态  
在设计 Class 的时候, 为了避免重复的数据和函数, 就会使用继承来让类形成一个树形的层级结构.  

继承也是为了实现多态而存在的. 多态: 不同的类具有相似的行为. 在 C++中可以使用虚函数声明同名的函数, 并在不同的类中进行不同的实现.
## 1.2 类的定义  
## 1.3 构造函数  
## 1.4 析构函数

