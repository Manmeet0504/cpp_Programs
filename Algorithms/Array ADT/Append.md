# Appending an element in an array

**Description** This program shows appending an element in an array using structure.

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
void append(A *arr, int x)
{
	if(arr->len < arr->size)
	{
		arr->a[arr->len++] = x;
	}
}
int main()
{
	A arr = {{2,4,6,8,10},20,5};
	cout<<"Before appending"<<endl;
	display(arr);
	cout<<"After appending"<<endl;
	append(&arr,12);
	display(arr);
}

```

**Run Code[](https://rextester.com/OIQO36422)**
