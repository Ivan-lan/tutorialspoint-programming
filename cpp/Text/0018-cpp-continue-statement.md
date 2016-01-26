# C++ continue 语句

C++ 中的 **continue** 语句有点像 **break** 语句。但它不是强迫终止，continue 会跳过当前循环中的代码，强迫开始下一次循环。

对于 **for** 循环，**continue** 语句会导致执行条件测试和循环增量部分。对于 **while** 和 **do...while** 循环，**continue** 语句会导致程序控制回到条件测试上。

### 语法

C++ 中 **continue** 语句的语法：

~~~
continue;

~~~

### 流程图

![C++ continue 语句](../../img/566e60bce8957.jpg)

### 实例

~~~
#include <iostream>
using namespace std;
 
int main ()
{
   // 局部变量声明
   int a = 10;

   // do 循环执行
   do
   {
       if( a == 15)
       {
          // 跳过迭代
          a = a + 1;
          continue;
       }
       cout << "a 的值：" << a << endl;
       a = a + 1;
   }while( a < 20 );
 
   return 0;
}

~~~

当上面的代码被编译和执行时，它会产生下列结果：

~~~
a 的值： 10
a 的值： 11
a 的值： 12
a 的值： 13
a 的值： 14
a 的值： 16
a 的值： 17
a 的值： 18
a 的值： 19

~~~