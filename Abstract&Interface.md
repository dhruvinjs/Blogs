Hello Everyone,
In this blog I will be explaining a very important topic regarding OBJECT ORIENTED Programming
SO You have read about abstract class in many but in this blog I will be explaining about Abstract in a very points 
explaining the points with the help of Code examples
So let's Start
So for understanding we will first explain what is abstraact methods
Abstract methods are generally methods which does'nt have any body will just have a method name 


Example=
**Class student{  
void settingExamPaper()**
{}
}
UseCase= When there different departments fo student like MCA BBA and for each subjects will be different for each class the implementation will be different so thats why abstract methods were introduced

Class will be declared as Abstract method when it will have some abstract Methods it is not neccessary to have abstract methods for the class to marked as abstract
 abstract class BankAcc
{
	BankAcc()
	{
	System.out.println("inside BankAcc()");	
	}
	abstract void withdrawl();
	
	void deposit(int amt)
	{
		System.out.println("what to deposit");
	}
    final void changePIN()
	{
		System.out.println("Logic to changePIN");
	}
}
class SavingAcc extends BankAcc
{
	 SavingAcc()
	{
        super();
	System.out.println("inside SavingAcc()");	
	}
	
	 void withdrawl(){
		System.out.println("inside withdrawl() of SavingAcc");
	 }
	void showInsRate()
	{
		System.out.println("Interest Rate ");
	}
}

As you can see only one method is abstract and the other methods are regular annd final

In abstract class the object cannot be created?
Why?
So as you can see in above example there are 2 classes one class is BankAccount 
Now whenever we want to open acc bank always asks us which Acc Saving or Salary
It does not asks that only bank acc
So thats why we do not want user to create only ban acc we want user to create Saving acc that why we can mark BankAcc as abstract class.
The other objective to use abstract class is that we can use the abstract methods because we don't know how deposit method will work with the Saving acc so we cant provide real implementation and we have marked it abstract so that Saving acc will define it properly

Abstract method can have constructor and as I mentioned abstract class cannot have any object so this constructor wil be used by the derived class by using the contructor chaining(will dive deeper into coming blogs)
By Constructor chaining we can multiple constructor This and Super keyword can be used for this appraoch

When a ordinary class has a abstract method then it is neccessary to mark that class abstract otherwise compile time error will occur.
class  AbstrctDemo
{
	public static void main(String[] args) 
	{
		SavingAcc ac=new SavingAcc();
		ac.withdrawl();
		ac.deposit(1000);
        ac.showInsRate();
	}
}
Notice we have created SavingAcc obj no BankAcc object just like i have mentioned above that abstract class will not have object

Now We will talk About the interfaces
Interfaace are somewhat similar to Abstract classes becasue interface are similar to abstract class
But in interfaces there are different rules like whenever we are implementing a interface we have to implement its every method
interface Animal
{
	void sound();
	void food();
	int cityID=1234;
	default void showOwnerName()
	{
		System.out.println("Owner : Mukesh ");
	}

}
class Dog implements Animal
{
   public void sound()
	{
		System.out.println("Dog Sound : Bark");
		//cityID++;
	}
	public void food()
	{
		System.out.println("Dog Food : veg+ Non Veg");
	}

	public void showOwnerName()
	{
		System.out.println("Owner : Mukesh ");
	}
}

class InterfaceDemo
{
	public static void main(String[] args) 
	{
		//Animal d=new Dog();
		
		Dog d=new Dog();
		d.sound();
		d.food();
		d.showOwnerName();
		
	}
}
Interfaces are pure abstract in nature becasue all the methods are always abstract and they have public access specifier means all methods does not have defination and it is necessary to use all methods
Always remember that the class are extended and interfaces are implemented and we can implement numerous interfaces

Next point is that the interface data members will be static mmenas shared by everyone and final means contant cannot chnage the value 
So thats why you can see that    public void sound()
	{
		System.out.println("Dog Sound : Bark");
		//cityID++;
	}
    commented line where i am changing the value of data member
    will give me error becasue i am trying to change the final data member value


//Animal d=new Dog();
It will work perfectly because in this we have created a Animal reference variable with a Dog object and this is not a object of animal the d will just hold a referncce of Dog object storerd in Heap memory
Note we can create refernce variable of abstract class but cannot create a object.
 

