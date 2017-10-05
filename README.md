# CircularLL
Circular Singly/ Doubly LinkedList

public class CircularSingly
{
	private Node head;
	private Node temp;
	private Node newNode;
	int data;
	Node next;

    private static class Node 
    {
        //int data;
        Node next;

        public Node(int data, Node next) 
        {
            this.data = data;
            this.next = next;
        }
    }
    
    public void insertAtFront(int value)
    {
		Node newNode = new Node(data, Node);
    	newNode.data = value;
    	if(head == null)
    	{
    		head = newNode;
    		newNode.next = head;
    	}
    	else
    	{
    		Node temp = head;
    		while(temp.next != head)
    		{
    			temp = temp.next;
    		}
    		newNode.next = head;
    		head = newNode;
    		temp.next = head;
    	}
    }
    
    public void insertAtEnd(int value)
    {
    	Node newNode = null;
    	newNode.data = value;
    	if(head == null)
    	{
    		head = newNode;
    		newNode.next = head;
    	}
    	else
    	{
    		Node temp = head;
    		while(temp.next != head)
    			temp = temp.next;
    		temp.next = newNode;
    		newNode.next = head;
    	}
    	
    }
    
    public void insertAfter(int value, int index)
    {
    	Node newNode;
    	newNode.data = value;
    	if(head == null)
    	{
    		head = newNode;
    		newNode.next = head;
    	}
    	else
    	{
    		Node temp = head;
    		while(temp.data != index)
    		{
    			if(temp.next == head)
    			{
    				System.out.println("Error"); // didn't work
    				return;
    			}
    			else
    			{
    				temp = temp.next;
    			}
    			newNode.next = temp.next;
    			temp.next = newNode; // success
    		}
    	}
    }
    
    public void deleteAtFront()
    {
    	if(head == null)
    	{
    		System.out.println("Linked List is empty");
    	}
    	else
    	{
    		Node temp = head;
    		if(temp.next == head)
    		{
    			head = null;
    		}
    	}
    }
    
    public void deleteAtEnd()
    {
    	if(head == null)
    	{
    		System.out.println("Linked List is empty");
    	}
    	else
    	{
    		Node temp1 = head , temp2;
    		if(temp1.next == head)
    		{
    			head = null;
    			return;
    		}
    		else
    		{
    			while(temp1.next != head)
    			{
    				temp2 = temp1;
    				temp1 = temp1.next;
    			}
    		}
    	}
    }

    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
}

