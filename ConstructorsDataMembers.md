**Understanding Java Fundamentals: Data Members, Constructors**

Now we’ll first understand about Data members

**In simple terms Data members are just properties/Attributes of an objects of class**

**This data members values are unique for every object**

Example

If we are talking about a student class of Mca

The properties of this class will be id (roll-no), Name, Gender, Email.

Now there are two types of data members in Oops concept

**Static vs. Non-Static Data Members**

- **Static data members:** Belong to the class itself and are shared by all objects of that class. They're declared using the static keyword.
- **Non-static data members:** Belong to individual objects and have a separate copy for each instance.

Code snippet to explain the static members and non-static members

class Student {

int id;

String name;

static String course = "MCA";

Student() {

System.out.println("In default constructor");

this.id = 0; // Using 'this' to explicitly refer to the instance variable

this.name = "";

}

Student(int id, String name) {

this.id = id;

this.name = name;

}

public class Main {

public static void main(String[] args) {

Student s1=new Student();

Student s2=new Student(105,”Gangadhar”);

System.out.println(s1);

System.out.println(s2);

}}

**Output:**

In default constructor

In parameterized constructor

Id=0, Name=, Course=MCA

Id=105, Name=Gangadhar, Course=MCA

Here in the above code snippet we can see that the even if we don’t pass the value the copy of **static data member course** is automatically **MCA**

Now Let’s come to our next topic

**Constructor**

**Let’s understand it from Above code**

**Rules and chartacteristics**

- **Don’t have a return type**
- **Should have a same name as class**
- **It gets called when we create an object of class**

**Types of constructors**

**Default Constructor**

Let’s understand this from above code snippet

When u don’t give any value when creating a object it gets called

Example=not given any value to s1 object therefore default constructor

Is called and also you can see I have a print statement in default constructor

For easy understanding

**Parameterized constructor**

This is the second type of constructor in java

When we are passing any value to the object this constructor gets invoked

Example form above code=

S2 object has values so therefore the parameterized constructor is getting called

**Note**

**Class student{  
void student()**
{}
}

In this above code you can see a method

You may confuse it and assume that it is a constructor but no

It is just a **member function** with void return type

Just as the characteristics mentioned above

**The constructors don’t have a return type**

Java allows you to create this method with a same name,

But do not assume it is a constructor.

**Also it is a bad practice to name this method with same name as class**

**It creates ambiguity and confusion so avoid it**

**The this Keyword**

The this keyword is a reference to the current object. It's often used to:

- **Resolve ambiguity:** When a local variable has the same name as an instance variable, this can be used to refer to the instance variable.

**Key Points:**  
Data members contain the unique attributes of objects.  
Static data members are shared by all objects in a class, whereas non-static data members are specific to each object.  
Constructors are used to initialize objects.  
This keyword relates to the current object and can be used to resolve ambiguity, invoke constructors, and return the object.  
Next article:  
In the next article, we'll dive further into this term and its different applications in Java programming.
