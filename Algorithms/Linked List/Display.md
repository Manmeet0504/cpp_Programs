# Creation and display of linked list

**Description :** This program shows the creation and display of linked list

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
	for(int i=1;i<n;i++)
	{
		t=new node;
		t->data=a[i];
		t->next=NULL;
		last->next=t;
		last=t;
	}
}
void display(node *p)
{
	while(p!=NULL)
	{
		cout<<p->data<<"->";
		p=p->next;
		if(p==NULL)
		{
			cout<<"NULL";
		}
	}
}
int main()
{
	int a[]={2,4,6,8,10};
	create(a,5);
	display(first);
}
```

**Run Code[](https://rextester.com/TUYRM24639)**
