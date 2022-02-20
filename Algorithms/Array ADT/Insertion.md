# Inserting an element in an array

**Description :** This program shows inserting an element in an array using structure.

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
void insert(A *arr,int index, int value)
{
	if(index>=0 && index<= arr->len)
	{
		for(int i=arr->len;i>index;i--)
		{
			arr->a[i]=arr->a[i-1];
		}
		arr->a[index]=value;
		arr->len++;
	}
}
int main()
{
	A arr = {{2,4,6,8,10},20,5};
	cout<<"Before inserting"<<endl;
	display(arr);
	cout<<"After inserting"<<endl;
	insert(&arr,5,12);
	display(arr);
}
```

**Run Code[](https://rextester.com/KUQPL90043)**
