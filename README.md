# Customer_Bank_Application_Java8
Bank Operation , Cerdit, 

git remote add origin https://github.com/AKSHAY123-AKS/bank_customer_Application_Java.git
git branch -M main
git push -u origin main
ASSIGNMENT NO 4.1
1->Create a java applicstion for the following.
 Create a Customer class , with data members (all private : tight encapsulation)
name(String),email(String),age(int), creditLimit(double)
4.1 Supply a parameterized constructor to accept all details from user
4.2 Supply an argument less  constructor to init default name to "Riya" , email to "riya@gmail.com",age=25,creditLimit=10000
(Must use constructor chaining)
4.3 Write a method , getDetails to return String form of customer name & credit limit only.
4.4 Supply getter & setter for creditLimit.
Naming convention : public void setCreditLimit(double limit) {...}
public double getCreditLimit(){...}
4.5 Create a TestCustomer class . Use scanner to accept user i/ps.
Create 2 customers using 2 different constructors(4.1 : customer1 ,4.2 : customer2)
Display customer details of both customers.
Prompt user , for changing creditLimit of the customer2.
Display new credit limit on the console.

CUSTOMER
import java.util.Scanner;
public class Customer 
{
	private String name,email;
	private int age;
	private double creditlimit;
	
	Scanner sc=new Scanner(System.in);
	public Customer()
	{
		name="Riya";
		email="riya@gmail.com";
		age=25;
		creditlimit=10000;
	}
	
	public Customer(String name,String email,int age,double creditlimit)
	{
		this.name=name;
		this.email=email;
		this.age=age;
		this.creditlimit=creditlimit;
	}
	
	public void getDetails()
	{
		System.out.println("Name="+name);
		System.out.println("Age="+age);
		System.out.println("Email="+email);
		System.out.println("Credit Limit="+creditlimit);
	}
	
	
	public void setCreditLimit()
	{
		System.out.println("Enter new Credit Limit=");
		creditlimit=sc.nextDouble();
	}
	public double getCreditLimit()
	{
		return creditlimit;
	}

}


TESTCUSTOMER
public class TestCustomer 
{
	public static void main(String[] args) 
	{
		Customer testc=new Customer();
		System.out.println("----------------------------");
		System.out.println("DEFAULT VALUES");
		testc.getDetails();
		System.out.println("----------------------------");
		Customer c1=new Customer("Gaurav","gapte00@gmail.com",23,50000);
		c1.getDetails();
		System.out.println("----------------------------");
		Customer c2=new Customer("Darshan","darshan@gmail.com",24,70000);
		c2.getDetails();
		System.out.println("----------------------------");
		c2.setCreditLimit();
		double c=c2.getCreditLimit();
		System.out.println("New Credit Limit of customer 2="+c);	
		System.out.println("----------------------------");
		c2.getDetails();
		System.out.println("----------------------------");
	}
}




OUTPUT
----------------------------
DEFAULT VALUES
Name=Riya
Age=25
Email=riya@gmail.com
Credit Limit=10000.0
----------------------------
Name=Gaurav
Age=23
Email=gapte00@gmail.com
Credit Limit=50000.0
----------------------------
Name=Darshan
Age=24
Email=darshan@gmail.com
Credit Limit=70000.0
----------------------------
Enter new Credit Limit=
80000
New Credit Limit of customer 2=80000.0
----------------------------
Name=Darshan
Age=24
Email=darshan@gmail.com
Credit Limit=80000.0
----------------------------
