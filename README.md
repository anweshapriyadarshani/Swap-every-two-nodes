# Swap-every-two-nodes
Given the head of a singly linked list, swap every two nodes and return its head.  For example, given 1 -> 2 -> 3 -> 4, return 2 -> 1 -> 4 -> 3


#include<bits/stdc++.h>
using namespace std;
class node
{
	public:int data;
	node *next;
};
//function to pairwise swap elements
void pairwiseswap(node *head)
{
	node *temp=head;
	//traverse if there are exactly two nodes left
	while(temp!=NULL && temp->next=NULL)
	{
		//swap data of the node with next node
		swap(temp->data,temp->next->data);
		//move temp by 2 for next pair
		temp=temp->next->next;
	}
}
//function to add node in the beginning of the list
void push(node** headref, int newdata)
{
	//allocate node
	node* newnode=new node();
	//enter data into node
	newnode->data=newdata;
	//link the old list to new node
	newnode->next=(head*ref);
	//move the new node to new node
	(*headref)=newnode;
	//function to print nodes in a given linked list
	void printlist(node* node)
	{
		while(node!=NULL)
		{
			cout<<node->data<<" ";
			node=node->next;
		}
	}
	//driver code
	int main()
	{
		node *start=NULL;
		push(&start,5);
		push(&start,4);
		push(&start,3);
		push(&start,2);
		push(&start,1);
		cout<<"linked list before calling pairwise swap";
		printlist(start);
		pairwiseswap(start);
		cout<<"linked list after calling pairwise swap";
printlist(swap);
return 0;
	}		
	
	
	
		
