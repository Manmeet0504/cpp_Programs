# Linear Search in Linked List

**Description :** This program shows linear search in linked list

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
	cout<<endl;
}

node* linear_search(node *p,int key)
{
	while(p!=NULL)
	{
		if(p->data==key)
		{
			return p;
		}
		p=p->next;
	}
	return 0;
}
int main()
{
	int a[]={2,4,6,8,10};
	node *t = new node;
	create(a,5);
	display(first);
	t = linear_search(first,6);
	if(t->data!=NULL)
	{
		cout<<"Value found i.e. "<<t->data<<endl;
	}
}

```

**Run Code[](https://rextester.com/QGSZO75275)**
