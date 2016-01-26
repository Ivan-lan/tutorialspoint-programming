# C++ 嵌套 switch 语句

您可以把一个 **switch** 作为一个外部 **switch** 的语句序列的一部分，即可以在一个 **switch** 语句内使用另一个 **switch** 语句。即使内部和外部 switch 的 case 常量包含共同的值，也没有矛盾。

C++ 中的 switch 语句允许至少 256 个嵌套层次。

### 语法

C++ 中 **嵌套 switch** 语句的语法：

~~~
switch(ch1) {
   case 'A': 
      cout << "这个 A 是外部 switch 的一部分";
      switch(ch2) {
         case 'A':
            cout << "这个 A 是内部 switch 的一部分";
            break;
         case 'B': // 内部 B case 代码
      }
      break;
   case 'B': // 外部 B case 代码
}

~~~

### 实例

~~~
#include <iostream>
using namespace std;
 
int main ()
{
   // 局部变量声明
   int a = 100;
   int b = 200;
 
   switch(a) {
      case 100: 
         cout << "这是外部 switch 的一部分" << endl;
         switch(b) {
            case 200:
               cout << "这是内部 switch 的一部分" << endl;
         }
   }
   cout << "a 的准确值是 " << a << endl;
   cout << "b 的准确值是 " << b << endl;
 
   return 0;
}

~~~

当上面的代码被编译和执行时，它会产生下列结果：

~~~
这是外部 switch 的一部分
这是内部 switch 的一部分
a 的准确值是 100
b 的准确值是 200

~~~