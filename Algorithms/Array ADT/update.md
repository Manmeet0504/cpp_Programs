# Updation of element

**Description :** This program shows updation in an array.

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
void update(A *arr,int index,int value)
{
	arr->a[index]=value;
}

int main()
{
	int ans,x,i,n;
	A arr = {{2,4,6,8,10},20,5};
	cout<<"Elements of array are:-"<<endl;
	display(arr);
	cout<<"Enter the index you want to update"<<endl;
	cin>>i;
	cout<<"Enter the new element"<<endl;
	cin>>n;
	update(&arr,i,n);
	display(arr);
}
```

**Run Code[](https://rextester.com/QGF39527)**
