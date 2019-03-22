---
Layout: 
Title: "LinkedList VS ArrayLinks"
Date: 2019-03-19 14:10
Categories:
---

# LinkedList VS ArrayLinks

Java ArrayList is perhaps the simplest and one of the most used data structure implementation classes of the Java API Library. It is a part of the Java Collection Framework under the java.util package.it is a generic re-sizable collection implementation of the List interface. Java ArrayList is especially used for managing a large number of objects.

Java ArrayList uses an array as the internal programming construct to store elements. An array is nothing but a sequential collection same type of elements, accessed by their index values. Naturally, Java ArrayList also behaves in a similar manner.

ArrayList is implemented as a resizable array. As more elements are added to ArrayList, its size is increased dynamically. It's elements can be accessed directly by using the get and set methods, since ArrayList is essentially an array. LinkedList is implemented as a double linked list. Its performance on add and remove is better than Arraylist, but worse on get and set methods. Vector is similar with ArrayList, but it is synchronized.

## Example ArrayList

ArrayList al = new ArrayList();
al.add(3);
al.add(2);
al.add(1);
al.add(4);
al.add(5);
al.add(6);
al.add(6);

Iterator iter1 = al.iterator();
while(iter1.hasNext()){
System.out.println(iter1.next());
}

# LinkedList

LinkedList is implemented as a double linked list. Its performance on add and remove is better than Arraylist, but worse on get and set methods. Manipulation with LinkedList is faster than ArrayList because it uses a doubly linked list, so no bit shifting is required in memory.

LinkedList class can act as a list and queue both because it implements List and Deque interfaces. Is better for manipulating data.

## Example LinkedList

    import java.util.*;    
    class TestArrayLinked{    
     public static void main(String args[]){    
            
        
      List<String> al2=new LinkedList<String>();//creating linkedlist    
      al2.add("James");//adding object in linkedlist    
      al2.add("Serena");    
      al2.add("Swati");    
      al2.add("Junaid");    
        
      System.out.println("linkedlist: "+al2);  
     }    
    }    

