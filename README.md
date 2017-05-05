# Stack-Using-Linked-List

public class STCKNode {
	
	public int data;
	public STCKNode next;

}

public class StackLinkList {

	private STCKNode top;
	
	public StackLinkList() {
		top = null;
	}
	
	public void pushIt(int data) {
		//create new node
		STCKNode newnode = new STCKNode();
		newnode.data = data;
		newnode.next = null;
		
		if (top == null) top = newnode; //it fits first place because list is empty
		else {
			//i want find top node 
			newnode.next = top;
			
			top = newnode;
		}
	}
	
	public void pullIt() {
		STCKNode p=top;
		top = p.next;
	}
	
	public void printIt() {
		STCKNode p=top;
		System.out.print("TOP--> ");
		while (p!=null) {
			System.out.print(p.data + " --> ");
			p = p.next;
		}
		System.out.println("\n");
	}
}
