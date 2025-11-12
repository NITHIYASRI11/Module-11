   # 📚 Singly Linked List : Find the Middle Node of a Singly Linked List Using Recursion

This Python program demonstrates how to find the middle node of a singly linked list using recursion. The program calculates the middle element by utilizing two pointers, with one pointer moving one step at a time (slow) and the other moving two steps at a time (fast). When the fast pointer reaches the end of the list, the slow pointer will be at the middle node.

## 🎯 Aim

To write a Python program that:
- Creates a singly linked list.
- Uses recursion to find the middle node of the list.
- In case of an even number of nodes, it returns the second middle element.

## 🧠 Algorithm

1. **Node Class**: 
   - Define a `Node` class to represent each node in the singly linked list. Each node has two attributes: `data` and `next`.
   
2. **LinkedList Class**:
   - Define a `LinkedList` class that manages the linked list with methods to:
     - `append(data)`: Add a new node to the end of the list.
     - `get_middle_recursive(slow, fast)`: A recursive helper function to find the middle node using two pointers (slow and fast).
     - `find_middle()`: A method to call the recursive function and return the middle node's data.

3. **Input**:
   - First, the program reads an integer `n`, representing the number of elements in the linked list.
   - Then, it reads `n` space-separated integers to form the linked list.

4. **Recursive Middle Finding**:
   - The `get_middle_recursive` method uses two pointers to traverse the list:
     - The `slow` pointer moves one step at a time.
     - The `fast` pointer moves two steps at a time.
   - When the `fast` pointer reaches the end, the `slow` pointer will be at the middle node.

5. **Output**:
   - The program prints the middle element. If the list has an even number of nodes, it returns the second middle element.

---

## 💻 Program
      class Node:
          def __init__(self, data):
              self.data = data
              self.next = None
      
      def find_middle(head, fast=None, slow=None):
          if fast is None:
              fast = slow = head
              if not head:
                  return None
          if fast.next is None or fast.next.next is None:
              return slow
          return find_middle(head, fast.next.next, slow.next)
      
      # Create linked list: 1->2->3->4->5
      head = Node(1)
      head.next = Node(2)
      head.next.next = Node(3)
      head.next.next.next = Node(4)
      head.next.next.next.next = Node(5)
      
      middle = find_middle(head)
      print(middle.data if middle else None)
## Sample Input & Output
![image](https://github.com/user-attachments/assets/c6fcbc9a-a11c-4155-8026-356be6df329b)


## Result
Thus, the program that Creates a singly linked list, Uses recursion to find the middle node of the list, In case of an even number of nodes, it returns the second middle element is executed and verifies successfully.
