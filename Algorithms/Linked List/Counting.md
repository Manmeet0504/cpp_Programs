# Counting of elements in linked list

**Description :** This program shows the counting of elements in linked list

**Example**

```cpp
struct node
{
	int data;
	node *next;
}*first=NULL;
void create(int a[],int n)
{
	node *t,*last;
	first = new node;
	first->data=a[0];
	first->next=NULL;
	last=first;
	for(int i=0;i<n;i++)
	{
		t=new node;
		t->data=a[i];
		t->next=NULL;
		last->next=t;
		last=t;
	}
}
int count(node *p)
{
	if(p==0)
	{
		return 0;
	}
	else
	{
		return count(p->next)+1;
	}
}
int main()
{
	int a[]={2,4,6,8,10};
	create(a,5);
	cout<<"Total values "<<count(first);
}
```

**Run Code[](https://rextester.com/WOSSBJ62875)**
