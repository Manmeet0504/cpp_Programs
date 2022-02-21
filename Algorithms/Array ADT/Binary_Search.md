# Binary Search

**Description :** This program shows binary search in an array.

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
int binaryS(A *arr,int value)
{
	int beg=0,last=arr->len-1,mid;
	while(beg<=last)
	{
		mid=(beg+last)/2;
		if(arr->a[mid]==value)
		{
			return mid+1;
		}
		else if(arr->a[mid]>value)
		{
			last=mid-1;
		}
		else
		{
			beg=mid+1;
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
	ans = binaryS(&arr,x);
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

**Run Code[](https://rextester.com/NAAP90361)**
