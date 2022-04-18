# Deleting a node from a Linked List

**Description :** This program shows Deleting a node from a Linked List

**Example**

```cpp

struct node
{	int data;
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
int Delete(node *p,int index)
{
	int x;
	node *q;
	if(index == 0)
	{
		q=first;
		x=first->data;
		first=first->next;
		delete(q);
		return x;
	}
	else
	{
		for(int i=0;i<index-1;i++)
		{
			q=p;
			p=p->next;
		}
		q->next = p->next;
		x=p->data;
		delete(p);
		return x;
	}
}
int main()
{
	int a[]={2,4,6,8,10};
	node *t = new node;
	create(a,5);
	display(first);
	Delete(first,2);
	display(first);
}

```

**Run Code[](https://rextester.com/CRNZ89808)**
