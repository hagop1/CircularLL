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
    			temp = temp.next;
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
    
    
   /* public void insert(int data) 
    {
        Node newNode = new Node(data, null);
        if (head == null) 
        {
            head = newNode;
            head.next = head;
        } 
        else 
        {
            Node curr = head;
            do 
            {
                if (((curr.data <= data) && (curr.next.data >= data)) || curr.next == head)  
                {
                    newNode.next = curr.next;
                    curr.next = newNode;
                    if (data < head.data) 
                    {
                        head = newNode;
                    }
                    return;
                }
                curr = curr.next;
            } while (curr != head);
        }
    }*/
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
}
