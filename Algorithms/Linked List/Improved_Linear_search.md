# Improved Linear search in Linked List

**Description :** This program shows Improved Linear search i.e. moving the found node on the first position.

**Example**

```cpp

#include<iostream>
using namespace std;
class node
{
	private:
		//int data;
		node *next;

	public:
		int data;
		void create(int a[],int n);
		void display(node *p);
		int count(node *p);
		node* improved_linear_search(node *p,int key);

}*first=NULL;

void node::create(int a[],int n) // TO CREATE THE Linked List
{
	node *t , *last;
	first = new node;
	first->data=a[0];
	first->next=NULL;
	last=first;

	for(int i=1;i<n;i++)
	{
		t = new node;
		t->data=a[i];
		t->next=NULL;
		last->next=t;
		last=t;
	}
}

void node::display(node *p) // Display the Linked List
{
	while(1)
	{
		cout<<p->data<<"->";
		p=p->next;
		if(p==NULL)
		{
			cout<<"NULL"<<endl;
			break;
		}
	}
}

int node::count(node*p) // To count number of nodes in Linked List
{
	int c=0;
	while(p!=NULL)
	{
		c++;
		p=p->next;
	}
	return c;
}

node* node::improved_linear_search(node *p,int key)
{
	node *q;
	while(q!=NULL)
	{
		if(p->data==key)
		{
			q->next=p->next;
			p->next=first;
			first=p;
			return p;
		}
		else
		{
			q=p;
			p=p->next;
		}
	}
	return NULL;
}

int main()
{
	int a[]={1,2,3,4,5};
	node obj;
	node *d;
	d = new node;
	obj.create(a,5);
	obj.display(first);
	cout<<"Number of nodes "<<obj.count(first)<<endl;
	cout<<"Linear search in a Linked List"<<endl;
	d = obj.improved_linear_search(first,2);
	if(d==NULL)
	{
		cout<<"Not present"<<endl;
	}
	else
	{
		cout<<"Element found i.e. "<<d->data<<endl;
	}
	obj.display(first);
	return 0;
}

```

**Run Code[](https://rextester.com/AKOH52761)**
