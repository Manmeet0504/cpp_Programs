# Linear Searching in an array

**Description :** This program shows linear searching of an element in an array.

**Example**

```cpp

struct A
{
	int a[20];
	int size;
	int len;
};
void display(A arr)
{
	cout<<"ELEMENTS :-"<<endl;
	for(int i=0;i<arr.len;i++)
	{
		cout<<arr.a[i]<<" ";
	}
	cout<<endl;
}
int linerS(A *arr,int value)
{
	for(int i=0;i<arr->len;i++)
	{
		if(arr->a[i]==value)
		{
			return i+1;
		}
	}
	return -1;
}
int main()
{
	int ans,x;
	A arr = {{2,4,6,8,10},20,5};
	cout<<"Elements of array are:-"<<endl;
	display(arr);
	cout<<"Enter the value you want to search"<<endl;
	cin>>x;
	ans = linerS(&arr,x);
	if(ans == -1)
	{
		cout<<"Element is not present in the list"<<endl;
	}
	else
	{
		cout<<"Element found at position "<<ans<<endl;
	}
}

```

**Run Code[](https://rextester.com/MGR22032)**
