# Deleting an element in an array

**Description :** This program shows deleting an element in an array using structure.

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
void Delete(A *arr, int value)
{
	int i;
	for(i=0;i<arr->len;i++)
	{
		if(arr->a[i]==value)
		{
			break;
		}
	}
	for(;i<arr->len-1;i++)
	{
		arr->a[i]=arr->a[i+1];
	}
	arr->len--;
}
int main()
{
	A arr = {{2,4,6,8,10},20,5};
	cout<<"Before deleting"<<endl;
	display(arr);
	cout<<"After deleting"<<endl;
	Delete(&arr,8);
	display(arr);
}

```

**Run Code[](https://rextester.com/MEX12562)**
