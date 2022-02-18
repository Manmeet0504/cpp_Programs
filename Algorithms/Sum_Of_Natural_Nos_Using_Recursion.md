# Finding factorial using recursion

**Description** This program shows factorial using recursion.

**Example**

```cpp

int sum(int n)
{
	if(n>0)
	{
		return (sum(n-1)+n);
	}
}

int main()
{
	int a=10;
	cout<<sum(a);
}

```

**Run Code[](https://rextester.com/CLH92043)**
