# Left Rotate

**Description :** This program shows left rotate in an array.

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
void leftRotate(A *arr)
{
	int i,temp;
    temp = arr->a[0];
	for(i=0;i<arr->len-1;i++)
	{
		arr->a[i]=arr->a[i+1];
	}
	arr->a[i]=temp;
}

int main()
{
	int ans,x;
	A arr = {{2,4,6,8,10},20,5};
	cout<<"Elements of array are:-"<<endl;
	display(arr);
	cout<<"After left shift"<<endl;
	leftRotate(&arr);
	display(arr);
}
```

**Run Code[](https://rextester.com/BUCXZ18669)**
