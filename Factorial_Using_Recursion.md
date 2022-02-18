# Finding factorial using recursion

**Description** This program shows factorial using recursion.

**Example**

```cpp

#include<iostream>
using namespace std;

int fact(int n)
{
	if(n==0 || n==1)
	{
		return 1;
	}
	else
	{
		return (fact(n-1)*n);
	}
}

int main()
{
	int a=5;
	cout<<fact(a);
}

```

**Run Code[](https://rextester.com/RQFJX79774)**
