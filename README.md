# -
C++
### 2.23
定义
因为void*是一种特殊的指针类型，可用于存放任意对象的地址。而lp是一个长整型指针，i是一个普通整型，类型不匹配。
### 2.25
(a) ip是整型指针，值是所指数的指针前应该先初始化指针，若没有对象可以指，把指针p初始化为0。
### 2.24
地址，i是整型数，r是引用，r的值就是i的值。、
### 2.35
```
#include<iosream>
#include<typeinfo>

int main()
{
    const int i = 42;
    auto j = i;
    const auto &k = i;
    auto *p = &i;
    const auto j2 = i, &k2 = i;
    std::cout << typeid(i).name() << std::endl;
    std::cout << typeid(j).name() << std::endl;
    std::cout << typeid(k).name() << std::endl;
    std::cout << typeid(p).name() << std::endl;
    std::cout << typeid(j2).name() << std::endl
    return 0;
}
```
### 3.4
```
#include <iostream>
#include <string>
using namespace std;
void main()
{	
	string string1,string2;
	cin >> string1 >> string2;
	if (string1 != string2)
	{
		cout << (string1 >= string2 ? string1 : string2) << endl;
	}	
    else
    {
        cout << "same" << endl;
    }
}
```
### 3.5
```
#include <iostream>
#include <string>
using namespace std;
void main()
{	
	string string;
	string sumstring;
	while (getline(cin ,string))
	{
		sumstring = sumstring+string+" ";
		cout<<sumstring<<endl;
	}
}
```
### 3.20
```
#include <iostream>
#include <string>
#include <vector>
using namespace std;
void main()
{	
	vector<int> my_vector;
	int a[10];
	for (int i = 0;i<10;i++)
	{
		cin>>a[i];
	}
	for (int j = 0;j<10;j++)
	{
		my_vector.push_back(a[j]);
	}
	int sum[10];
	for (int k = 0;k<5;k++)
	{
		sum[k] = my_vector[k] + my_vector[9-k];
		cout<<sum[k]<<endl;
	}
} 
```
### 3.23
```
#include <iostream>
#include <string>
#include <vector>
using namespace std;
void main()
{	
	vector<int> text(10,5);
	for (auto it = text.begin(); it != text.end();it++)
	{
		*it = *it * 2;
		cout<<*it<<endl;	
	}
} 
```
### 6.10
```
#include <iostream>
#include <string>
#include <vector>
using namespace std;
int exchange(int &val1, int &val2)
{
	int a;
	a = val1;
	val1 = val2;
	val2 = a;
	return 0;
}
void main()
{	
	cout<<"输入两整数:";
	int val1,val2;
	cin>>val1>>val2;
	cout<<"交换前"<<val1<<" "<<val2<<endl;
	exchange(val1,val2);
	cout<<"交换后"<<val1<<" "<<val2<<endl;
}
```
### 6.19
(a)非法，函数只包含一个参数，a有两个参数
(b)(c)(d)合法

### 6.39
(a)第二条语句非法。顶层const不影响传入函数的对象，所以一个拥有顶层const的形参无法与另一个没有顶层const的形参区分。
(b)第二条语句非法。重载函数必须在形参数量或形参类型上有所区别。

### 7.16
在类的定义中，可以包含0个或多个访问说明符，并且对次数和位置没有严格限定。
一般构造函数和一部分成员函数应该定义在public说明符后，数据成员和作为实现部分的函数应该跟在private说明符后。

### 7.49
(a)编译器用string对象s自动创建Sales_data对象，然后传给combine的形参，函数正确执行并返回结果。
(b)无法编译通过
(c)无法编译通过
