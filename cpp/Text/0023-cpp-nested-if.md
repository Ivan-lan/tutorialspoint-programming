# C++ 嵌套 if 语句

在 C++ 中，**嵌套** if-else 语句是合法的，这意味着您可以在一个 **if** 或 **else if** 语句内使用另一个 **if** 或 **else if** 语句。

### 语法

C++ 中 **嵌套 if** 语句的语法：

~~~
if( boolean_expression 1)
{
   // 当布尔表达式 1 为真时执行
   if(boolean_expression 2)
   {
      // 当布尔表达式 2 为真时执行
   }
}

~~~

您可以嵌套 **else if...else**，方式与嵌套 *if* 语句相似。

### 实例

~~~
#include <iostream>
using namespace std;
 
int main ()
{
   // 局部变量声明
   int a = 100;
   int b = 200;
 
   // 检查布尔条件
   if( a == 100 )
   {
       // 如果条件为真，则检查下面的条件
       if( b == 200 )
       {
          // 如果条件为真，则输出下面的语句
          cout << "a 的值是 100，且 b 的值是 200" << endl;
       }
   }
   cout << "a 的准确值是 " << a << endl;
   cout << "b 的准确值是 " << b << endl;
 
   return 0;
}

~~~

当上面的代码被编译和执行时，它会产生下列结果：

~~~
a 的值是 100，且 b 的值是 200
a 的准确值是 100
b 的准确值是 200

~~~