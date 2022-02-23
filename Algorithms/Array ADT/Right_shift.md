# Right Shift

**Description :** This program shows right shift in an array.

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
void rightShift(A *arr)
{
	int i;
	for(i=arr->len;i>0;i--)
	{
		arr->a[i]=arr->a[i-1];
	}
	arr->a[0]=0;
}

int main()
{
	int ans,x;
	A arr = {{2,4,6,8,10},20,5};
	cout<<"Elements of array are:-"<<endl;
	display(arr);
	cout<<"After left shift"<<endl;
	rightShift(&arr);
	display(arr);
}
```

**Run Code[](https://rextester.com/FSRUP45227cd)**
