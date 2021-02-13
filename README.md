## 使用C++语言实现[B站王卓老师的数据结构公开课课程代码](https://www.bilibili.com/video/BV1nJ411V7bd?p=1)


### 文章目录

**1-基础概念**

- [思维导图笔记](https://www.processon.com/view/link/601d43ad5653bb053e33e231)

**2-数据结构代码实现**

- [线性表](https://github.com/IRVING-L/Algorithm_fromBilibili/blob/main/%E7%BA%BF%E6%80%A7%E8%A1%A8.md)
- [栈、队列](https://github.com/IRVING-L/Algorithm_fromBilibili/blob/main/%E6%A0%88%E5%92%8C%E9%98%9F%E5%88%97.md)
- 串、数组、广义表
- [树](https://github.com/IRVING-L/DataStruct_fromBilibili/blob/main/%E4%BA%8C%E5%8F%89%E6%A0%91.md)
- [图](https://github.com/IRVING-L/DataStruct_fromBilibili/blob/main/%E5%9B%BE.md)

**3-算法代码实现**

- [查找算法](https://github.com/IRVING-L/DataStruct_fromBilibili/blob/main/%E6%9F%A5%E6%89%BE%E7%AE%97%E6%B3%95.md)
- [排序算法](https://github.com/IRVING-L/Algorithm_fromBilibili/blob/main/%E6%8E%92%E5%BA%8F.md)


### <span id="ch0">使用说明</span>  

**eg.1:**

~~~cpp
//ElemType是数据类型别名，常见的有：
typedef int ElemType;
~~~


**eg.2：**

~~~cpp
//王卓老师视频中常用的结构体定义方式
typedef struct{
    ElemType data[];
    int length;
}SqList; //顺序表类型
~~~

~~~cpp
//本文将使用以下struct定义方式
struct SqList
{
    ElemType data[];
    int length;
};
//或使用class定义一个类
class SqList
{
    ElemType data[];
    int length;
};
~~~

**eg.3：**

~~~c
//C语言中动态分配内存的函数：malloc
malloc(m);//开辟m字节长度的地址空间，返回这段地址的首地址
//王卓老师视频范例
#define MAXSIZE 100
typedef struct{
    ElemType *data;
    int length;
}SqList;
//...//
SqList L;
L.data = (ElemType*)malloc(sizeof(ElemType)*MAXSIZE);
~~~

~~~cpp
//本文将使用以下C++的动态内存分配方式：new
//使用new重写上面的malloc
L.data = new ElemType[MAXSIZE];
~~~

> 本人菜鸟一枚，欢迎大家闲暇时对代码或者总结提点Issue，笔芯
