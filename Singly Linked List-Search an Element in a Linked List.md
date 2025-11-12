# # 🔍 Singly Linked List-To Search an Element in a Linked List

This project contains a simple implementation of a **singly linked list** in Python, allowing insertion and searching of elements.

---

## 🎯 Aim

To write a Python program to search for a given element in a singly linked list using object-oriented programming principles.

---

## 🧠 Algorithm

1. **Define a Node class** with `data` and `next` attributes.
2. **Define a LinkedList class** with:
   - A `head` pointer initialized to `None`.
   - A `push()` method to add elements at the beginning.
   - A `search()` method to check whether a given value exists.
3. Create a `LinkedList` instance.
4. Insert the elements **10, 30, 11, 21, 14** using `push()` (which results in reverse order).
5. Read an integer input from the user.
6. Use `search()` to check if the element exists in the list.
7. Output **"Yes"** if found, else **"No"**.

---

## 💻 Program
      class Node:
        def __init__(self, data):
          self.data = data
          self.next = None
      
      class SinglyLinkedList:
        def __init__(self):
          self.head = None
      
        def push_back(self, newElement):
          newNode = Node(newElement)
          if(self.head == None):
            self.head = newNode
            return
          else:
            temp = self.head
            while(temp.next != None):
              temp = temp.next
            temp.next = newNode
      
        def Search(self, ele):
            cur=self.head
            i=0
            while cur!=None:
                i+=1
                if cur.data==ele:
                    return i
                cur=cur.next
            return False
          
        def show(self):
          temp = self.head
          print("The list elements are:", end=" ")
          while (temp != None):
              print(temp.data, end=" ")
              temp = temp.next
          print()
      
        def find_index(self,key):
              current_node=self.head
              index=0
              while current_node:
                  if current_node.data==target:
                      return index
                  
                       
      s = SinglyLinkedList()
      n=10
      
      while(n!=0):
          n=int(input("Enter your choice : \n"))
          if(n==1):
              s.push_back(int(input("Enter element to add : \n")))
          elif(n==0):
              break
          else:
              print("[INVALID INPUT]: try again")
              continue
      
      key = int(input("enter the element to search  into the linked list \n"))
      s.show()
      
      if s.Search(key):
          print(key,"is found at position ",s.Search(key))
      else:
          print(key,"is not found in the given linked list.")
## Sample Output
![image](https://github.com/user-attachments/assets/3e9b23a2-af53-48d4-b1ca-79751577cddc)

## Result
Thus, the program to search for a given element in a singly linked list using object-oriented programming principles is executed and verified successfully.
