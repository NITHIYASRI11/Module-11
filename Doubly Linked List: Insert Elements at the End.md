# 📚 Doubly Linked List: Insert Elements at the End of a Doubly Linked List

This Python program demonstrates the creation and manipulation of a **Doubly Linked List** where elements can be inserted at the **end** of the list. The program also provides a method to traverse the list and display the elements.

---

## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List**.
- Allows insertion of elements at the end of the list.
- Provides functionality to traverse the list and display its elements.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Node` to represent each node in the doubly linked list with attributes:
   - `item` for storing the data of the node.
   - `nref` for storing the reference to the next node.
   - `pref` for storing the reference to the previous node.

2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `start_node` to point to the first node of the list.

3. **Step 3:** Define methods in the `DoublyLinkedList` class:
   - `insert_in_emptylist(data)` to insert an element when the list is empty.
   - `insert_at_end(data)` to insert elements at the end of the list.
   - `traverse_list()` to traverse the list and print the elements.

4. **Step 4:** Create an instance of `DoublyLinkedList` and use the `insert_at_end()` method to insert elements into the list.

5. **Step 5:** Use the `traverse_list()` method to print the elements of the list.

---

## 💻 Program
      class Node:
          def __init__(self, data):
              self.item = data
              self.nref = None
              self.pref = None
      
      class DoublyLinkedList:
          def __init__(self):
              self.start_node = None
      
          def insert_in_emptylist(self, data):
              if self.start_node is None:
                  new_node = Node(data)
                  self.start_node = new_node
              else:
                  print("list is not empty")
                  
          def insert_at_start(self, data):
              if self.start_node is None:
                  new_node = Node(data)
                  self.start_node = new_node
                  print("node inserted")
                  return
              new_node = Node(data)
              new_node.nref = self.start_node
              self.start_node.pref = new_node
              self.start_node = new_node
              
          def insert_at_end(self, data):
              if self.start_node is None:
                  new_node = Node(data)
                  self.start_node = new_node
                  return
              n = self.start_node
              while n.nref is not None:
                  n = n.nref
              new_node = Node(data)
              n.nref = new_node
              new_node.pref = n
              
          def traverse_list(self):
              if self.start_node is None:
                  print("List has no element")
                  return
              else:
                  n=self.start_node
                  while n is not None:
                      print(n.item,' ')
                      n=n.nref
              
                      
      new_linked_list = DoublyLinkedList()
      new_linked_list.insert_in_emptylist(50)
      new_linked_list.insert_at_start(10)
      new_linked_list.insert_at_start(5)
      new_linked_list.insert_at_start(18)
      new_linked_list.insert_at_end(29)
      new_linked_list.insert_at_end(39)
      new_linked_list.insert_at_end(49)
      new_linked_list.traverse_list()
        


## Sample Output
![image](https://github.com/user-attachments/assets/ed9ccaa1-408b-40d9-9f3b-a8ce570b317c)

## Result
Thus, the program that Implements a **Doubly Linked List**, Allows insertion of elements at the end of the list, Provides functionality to traverse the list and display its elements is executed and verified successfully.
