# Some more operations

**Description :** This program shows demonstration of get and set function using switch case

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
void set(A *arr,int n,int value)
{
	arr->a[n]=value;
}

int get(A arr,int n)
{
	return (arr.a[n]);
}

int main()
{
	int ans,x,i,n,a;
	A arr = {{2,4,6,8,10},20,5};
	cout<<"Elements of array are:-"<<endl;
	display(arr);
	cout<<"Enter your choice"<<endl;
	cout<<"1. Set a new value"<<endl;
	cout<<"2. Get a value"<<endl;
	cin>>a;
	switch(a)
	{
		case 1 :
			{
				int p,q;
				cout<<"Enter the index you want to change"<<endl;
				cin>>p;
				cout<<"Enter the new value"<<endl;
				cin>>q;
				set(&arr,p,q);
				cout<<"Updated array"<<endl;
				display(arr);
				break;
			}
		case 2 :
			{
				int p;
				cout<<"Enter the index you want"<<endl;
				cin>>p;
				cout<<"Element is ";
				cout<<get(arr,p);
				break;
			}
	}
}
```

**Run Code[](https://rextester.com/CRJA60603)**
