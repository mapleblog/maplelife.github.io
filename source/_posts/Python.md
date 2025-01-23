---
title: Python Basic
date: 2024-12-04 10:16:49
categories:
- Skill
- Python
tags:
---

# Introduction
**

# Types of Databases
* String	字符串
* Integer	整数
* Float		浮点数
* Boolean	布尔值
* Tuple		元组
* List		列表
* Dictionary	字典
* Set		集合

---

# If...Else
*Conditions and If statements*
Python supports the usual logical conditions from mathematics:
* Equals: a == b
* Not Equals: a != b
* Less than: a < b
* Less than or equal to: a <= b
* Greater than: a > b
* Greater than or equal to: a >= b

Example
If statement:
```shell
# Example
# If statement:

a = 33
b = 200
if b > a:
  print("b is greater than a")
```

      
*Indentation*
Python relies on indentation (whitespace at the beginning of a line) to define scope in the code. 
If statement, without indentation (will raise an error):

```shell
a = 33
b = 200
if b > a:
print("b is greater than a") # you will get an error
```  


# Functions (函数)
自定义函数如果没有指定返回结果，默认返回空值None。
如果返回指定的数据如字典，列表，字符串，整数，浮点数 就可以对它们进行处理

如返回的数据是字典就会赋值给变量，
该变量就可以进行字典的处理  

**位置参数 (args)**
* *args：接收任意数量的 位置参数” 参数会被作为一个元组传递给函数。 
* *是语法标记，args 是约定的名字，可以用其他名称代替（如 *params），但 *args 是社区推荐的写法。 

**关键字参数 (kwargs)**
* **kwargs 允许函数接受任意数量的 关键字参数，参数会被作为一个字典传递给函数。
* **是语法标记，kwargs 是约定的名字，也可以用其他名称代替（如 **options）  


# For Loops (for 循环)
  


# While Loops (while 循环)


