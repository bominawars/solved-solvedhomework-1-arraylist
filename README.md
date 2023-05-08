Download Link: https://assignmentchef.com/product/solved-solvedhomework-1-arraylist
<br>
Problem I.

In this handout you have the 3 files that are part of your homework, the expected output and some style guidelines.

The 3 files are ArrayList, that emulates an array list, the interface List, and a driver that tests ArrayList.Your job is to write the missing methods of ArrayList.The header comments of the methods are the guidelines.

I. The class ArrayList

import java.util.NoSuchElementException;

// the array list is implemented as the initial// segment [0:size-1] of arr

public class ArrayList {// the initial size of arrprivate static final int INIT = 3;private int size = 0; // the size of the array listprivate T[] arr; // the array

// construct an empty array listpublic ArrayList(){arr = (T[]) new Object[INIT];

}

// insert the value v at index i// if i is out of index, throw an index out of bounds// exception. If the arr is full, create an array of twice// the size of arr, copy arr onto the new array and make// the new array the object array// Then do the insertionpublic void add(int i, T v){// you write it}

// add in the last locationpublic void add(T v){// you write it}

// return the value at i// if i is out of bounds throw a no such element exceptionpublic T get(int i){// you write it}

// remove the value at i// if i is out of bounds throw a no such element exceptionpublic T remove(int i){// you write it}

// set the value at i to v return the old value// if i is out of bounds throw an array index out of bounds// exceptionpublic T set (int i, T v){// you write it}

// clear the array sets size to zeropublic void clear(){size = 0;}

// returns the sizepublic int size(){return size;}

// print the slice arr[0:size-1]public void printArray(){// you write it

}}

II. The List interface.

public interface List&lt;T{// add an itemvoid add(T item);// add at a given indexvoid add(int i, T item);// remove at a given indexT remove(int i);// get the value at a given indexT get(int i);// set the value at i to v// return the old valueT set(int i, T v);// clear the arrayvoid clear();// return the sizeint size();

}

III. The driver for ArrayList

import java.util.NoSuchElementException;public class ToyList{

public static void main(String[] args){System.out.println(“Testing the ArrayList”);System.out.println(“=====================

”);

System.out.println(“We form an array list of strings”);ArrayList System.out.println(“We add Papa Bill”);profs.add(“Papa Bill”);System.out.println(“We add Shrek, Grandpa and Tornado”);profs.add(“Shrek”);profs.add(“Grandpa”);profs.add(“Tornado”);System.out.println(“The list has: ” + profs.size() +” profs.”);System.out.println(“We add Ali Baba at index 1″);profs.add(1,”Ali Baba”);System.out.println(“We add Poco Pelo at index 3″);profs.add(3,”Poco Pelo”);System.out.println(“We print the array list.”);profs.printArray();

System.out.println(“At index 4 we have ” + profs.get(4));

try{System.out.println(“We try to insert Zorba at index 7.”);profs.add(7,”Zorba”);}catch(ArrayIndexOutOfBoundsException e){System.out.println(“We cannot do it.”);}

System.out.println(“We change the prof at 3 to Ming the Merciless”);String last = profs.set(3,”Ming the Merciless”);System.out.println(“Ming replaces ” + last + “.”);

System.out.println(“We remove the prof at 2”);last = profs.remove(2);

System.out.println(“We print the array list.”);profs.printArray();

try{System.out.println(“We try to remove the prof at index 6.”);last = profs.remove(6);}catch(NoSuchElementException e){System.out.println(“We cannot do it.”);}

System.out.println(“We clear the array list.”);profs.clear();profs.printArray();

System.out.println(“I hope that your program worked!”);}}

IV. The expected output of the driver.

The output must be the one below (except for the format of printArray).

Testing the ArrayList=====================

We form an array list of stringsWe add Papa BillWe add Shrek, Grandpa and TornadoThe list has: 4 profs.We add Ali Baba at index 1We add Poco Pelo at index 3We print the array list.

The array is:arr[0] = Papa Billarr[1] = Ali Babaarr[2] = Shrekarr[3] = Poco Peloarr[4] = Grandpaarr[5] = TornadoAt index 4 we have GrandpaWe try to insert Zorba at index 7.We cannot do it.We change the prof at 3 to Ming the MercilessMing replaces Poco Pelo.We remove the prof at 2We print the array list.

The array is:arr[0] = Papa Billarr[1] = Ali Babaarr[2] = Shrekarr[3] = Poco Peloarr[4] = Grandpaarr[5] = TornadoAt index 4 we have GrandpaWe try to insert Zorba at index 7.We cannot do it.We change the prof at 3 to Ming the MercilessMing replaces Poco Pelo.We remove the prof at 2We print the array list.

The array is:arr[0] = Papa Billarr[1] = Ali Babaarr[2] = Ming the Mercilessarr[3] = Grandpaarr[4] = TornadoWe try to remove the prof at index 6.We cannot do it.We clear the array list.The array is empty.I hope that your program worked!BUILD SUCCESSFUL (total time: 0 seconds)

II.

You are given the interface Queue shown below.

public interface Queue

// add an itemvoid add(AnyType item);// remove an item, throw NoSuchElementException if the queue is emptyAnyType remove();// get the first element without removing it// throw NoSuchElementException if the queue is emptyAnyType getFirst();// get the sizeint getSize();// check if the queue is emptyboolean isEmpty();// empty the queuevoid clear();}

Write a generic class CircularQueue that implements this interface asa circular queue. The class must have 3 private fields, the data array,and the indices f and r that point to the first and the last elementof the queue, in this order. You may use an extra field, the size ofthe queue.

The class has 2 constructors, one that takes as input the size of data,and one that uses a default size, in this case 3.

Add checks that there is space in data, i.e. size &lt; data.length.If not, add creates a new array with twice as many elements as data,copies the contents of data starting with location f and ending with r,onto the new array, starting with location 0.

Then, add performs the insertion at the end of the queue.If data is empty before the insertion, initialize f and r.

Recall that in a circular queue, both the front and the rear wrap arroundthe end of the data array.

remove() also checks that the queue has 1 item. If that is the case,return the item and empty the queue.

You must also write the public method

public void display()

that displays f, r, the contents of data and the size of the queue.

Use the test below to check your program.

public static void main(String[] args) {System.out.println(“Testing Queues”);System.out.println(“==============


”);

System.out.println(“We form a queue with the names Papa Bill, Mark,”+ ” Ali Baba.”);

CircularQueue profs.add(“Papa Bill”);profs.add(“Mark”);profs.add(“Ali Baba”);

System.out.println(“We add the names Shrek, Jeff the Chef, Hex”);profs.add(“Shrek”);profs.add(“Jeff the Chef”);profs.add(“Hex”);System.out.println(“The queue has ” + profs.getSize() + ” persons.”);System.out.println(“We delete 4 names.”);for (int i = 1; i &lt;= 4; i++)System.out.println(“The delete name is ” + profs.remove());

System.out.println(“The name on top is ” + profs.getFirst());System.out.println(“We delete 2 more names.”);for (int i = 1; i &lt;= 2; i++)System.out.println(“The delete name is ” + profs.remove());System.out.println(“Now, isEmpty() is ” + profs.isEmpty());

System.out.println(“We try to remove a name.”);try{String name = profs.remove();}catch (NoSuchElementException e){System.out.println(“We get a NoSuchElementException”);}

} // end main

The output must be the one beneath.Testing Queues==============

We form a queue with the names Papa Bill, Mark, Ali Baba.We add the names Shrek, Jeff the Chef, HexThe queue has 6 persons.We delete 4 names.The delete name is Papa BillThe delete name is MarkThe delete name is Ali BabaThe delete name is ShrekThe name on top is Jeff the ChefWe delete 2 more names.The delete name is Jeff the ChefThe delete name is HexNow, isEmpty() is trueWe try to remove a name.We get a NoSuchElementException

III. Some Style Guidelines———————

Start the program with the author blockbelow./* COURSE : COP 3530* Section : U03* Semester :* Instructor :* Author : (your name)* Assignment #: 1* Due date :* Description : Insert a 2-3 line description of the assignment***/

Recall that the names of classes and of the variables are nouns, and thenames of the methods are verbs. The variables and the methods use onlylower case letters except for the first letter of the words of a compoundword. The constants have only capital letters and the words are separatedby underscores. Put header comments to describe what the method does andend comments to describe the variables.You may use Eclipse, JCreator or Netbeans to develop your program.e-mail me the java file of the class. Do not turn in the driver, the interface,or the output.