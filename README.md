# Thursday-Lab-11-jan
package Anudip;

/*
 * WAP to accept a choice from the user and accordingly display the output
1:Accept no and check it is prime no or Not
2:Accept no and find out the SUM OF DIGIT (123 =1+2+3 =6)
3:Accept a no from the user and  display the fibonacci series(0 1 1 2 3 5 .....)
4:Accept no from user and check it is armstrong or not
5: Accept 5 no and find out the greatest
6:Display the Month
7:Make a Calculator 
 */

import java.util.Scanner;

public class Test1 
{

	public static void main(String[] args) 
	{
		//We are using scanner to get input from keyboard
		Scanner sc = new Scanner(System.in);
		/*ans is an varible which store yes or no which ask that we want continue to 
		 * check another program or not
		 */
		char ans;
		//we are using do-while loop so we can repeat it for n number of times 
		do
		{
			System.out.println("Enter 1:Accept no and check it is prime no or Not \r \n"
					+"Enter 2:Accept no and find out the SUM OF DIGIT (123 =1+2+3 =6) \r \n"
					+"Enter 3:Accept a no from the user and  display the fibonacci series(0 1 1 2 3 5 .....) \r \n"
					+"Enter 4:Accept no from user and check it is armstrong or not \r \n"
					+"Enter 5:Accept 5 no and find out the greatest \r \n"
					+"Enter 6:To display the Month \r \n"
					+"Enter 7:To display the calculator");
			
			//choice :to choose a no from given options
			int choice=sc.nextInt();
			/*using switch case so that we can make a choose for 
			 * which program we want to perform
			 */
			switch (choice) 
			{
			
				case 1:
					//num stands for number
					//
					System.out.println("1:Accept no and check it is prime no or Not");
					System.out.println("Enter a No to check Wether it is Prime or not...?");
					int num=sc.nextInt();
					boolean prime =true;
					boolean Prime_no=true;
		//using for loop because we want check that the given no is divisble by any no before itself or not			
						for(int i=2;i<num;i++)
							{
								if(num%i==0)
									{
										prime=false;
										break;
									}
							}
						
					if(prime==Prime_no)
					{
						System.out.println(num+"   It is a prime Number");
					}
					else
					{
						System.out.println(num+"   It is not a prime number");
					}
					//False means not a prime & true means it is a prime Number
					break;
				
				case 2:
					//temp is a variable in which we are going to store new value(which is % 10)
					System.out.println("Accept no and find out the SUM OF DIGIT (123 =1+2+3 =6)");
					System.out.println("Enter a number:");
					int number=sc.nextInt();
					int sum=0;
						while(number>0) 
							{
							int temp=number%10;
							sum=sum+temp;
							number=number/10;
							}
					System.out.println("the sum of digit will be : "+sum);
					break;
					
				case 3:
					System.out.println("Accept a no from the user and  display the fibonacci series(0 1 1 2 3 5 .....)");
					System.out.println("Enter a number :");
					//ft is first term that is 0 and st is second term that is 1 and tt is third term that is going tobe addition of ft and st
					//fib is the value that we are going to take from user(how  no of series of fibonacci ?)
				        	int fib = sc.nextInt();
				        	int ft = 0, st = 1, tt;
				           	System.out.print("Fibonacci Series: ");
					            for (int i = 1; i <= fib; i++)
				                   {
					                System.out.println(ft + " ");
					                tt = ft + st;
					                ft= st;
					                st = tt;
					            }
				           
				            break;
		
				case 4:
					System.out.println("Accept no from user and check it is armstrong or not");
					System.out.println("Enter a no to check whether it is armstong or not ? ");
					int numb=sc.nextInt();
					/*Og stands for Original value that we have got from the user
					 * we are using Og so that we cant lose the original value
					 */
					//total is variable which stores the total value which we will compare with Og
					//using rem as remainder which store a value after finding the % of a number 

					int total = 0,Og,rem;
					Og=numb;
					 while(numb>0)
						{
						 rem =numb%10;
						numb=numb/10;
						total= total + rem*rem*rem;
						}
					    if(Og==total)
					    {
					    	System.out.println("It is a armstrong");
					    }
					    else
					    {
					    	System.out.println("It is not a armstrong");
					    }
					     
					break;
				
			case 5:
				//we are accepting 5 number from no1 to no5 respectively
				System.out.println("Accept 5 no and find out the greatest");
				System.out.println("Enter 1st Number");
				int no1=sc.nextInt();
				System.out.println("Enter 2st Number");
				int no2=sc.nextInt();
				System.out.println("Enter 3st Number");
				int no3=sc.nextInt();
				System.out.println("Enter 4st Number");
				int no4=sc.nextInt();
				System.out.println("Enter 5st Number");
				int no5=sc.nextInt();
				/*	we are using & operator 
					here we are comparing each number with the other and
				    in &-operator gives true when all the values are true
					we are using else if ladder so we a specific condition is true
					 then that part of block will get executed
					 
				 */
				if(no1>no2 && no1>no3 && no1>no4 && no1>no5)
				{
					System.out.println("First no is greatest :" +no1);
				}
				else if(no2>no1 && no2>no3 && no2>no4 && no2>no5)
				{
					System.out.println("Second no is greatest : "+no2);
				}
				else if(no3>no1 && no3>no2 && no3>no4 && no3>no5)
				{
					System.out.println("Third no is greatest : "+no3);
				}
				else if(no4>no1 && no4>no2 && no4>no3 && no4>no5)
				{
					System.out.println("Second no is greatest : "+no4);
				}
				
				else if(no5>no1 && no5>no2 && no5>no3 && no5>no4)
				{
					System.out.println("Second no is greatest : "+no5);
				}
				break;
				
			case 6:
				//Here we are making a calendar Using Switch case 
				//where value 1 to 12 stands for Jan to dec respectively.
				
				System.out.println("Display the month");
				System.out.println("Enter the no between 1 to 12 :");
				int month_no=sc.nextInt();
				switch (month_no) {
					case 1:
						System.out.println("January"+"  It has  31 days");
						break;
					case 2:
						System.out.println("Februray"+"  It has  28 days");
						break;
					case 3:
						System.out.println("March"+" It has  31 days");
						break;
					case 4:
						System.out.println("April"+"  It has  30 days");
						break;
					case 5:
						System.out.println("May"+"  It has  31 days");
						break;
					case 6:
						System.out.println("June"+"  It has  3o days");
						break;
					case 7:
						System.out.println("July"+"  It has  31 days");
						break;
					case 8:
						System.out.println("August"+"  It has  31 days");
						break;
					case 9:
						System.out.println("September"+"  It has  30 days");
						break;
					case 10:
						System.out.println("October"+"  It has  31 days");
						break;
					case 11:
						System.out.println("November"+"  It has  30 days");
						break;
					case 12:
						System.out.println("December"+"  It has  31 days");
						break;

				default:
					System.out.println("Invalid No");
					break;
				}
				
				break;
				
			case 7:
				//for creating a calculator we are use switch case 
				System.out.println("Make a calculator");
				/*we are using double data type because in division of 2 number
				 *  we can't get value in points . while entering a number we can
				 *  store a number with point
				 */
				System.out.println("Enter First Number : ");
				double first_no=sc.nextDouble();
				System.out.println("Enter Second Number : ");
				double second_no=sc.nextDouble();
				//op stands for operator  and operator in calculator are +,-,/,*,%
				System.out.println("Enter a operator ");
				char op=sc.next().charAt(0);
				    switch (op)
				    {
				    //(+ and add) stands for addition of 2 number 
					case '+':
						{
							double add=first_no+second_no;
							System.out.println("Addition of two number : "+add);
						}
						
						break;
						//(- and sub) stands for subtraction of 2 number 
					case '-':
						{
							double sub=first_no-second_no;
							System.out.println("Subtraction of two number : "+sub);
						}
						
						break;
						//(* and Mul) stands for multiplication of 2 number 
					case '*':
						{
							double Mul=first_no*second_no;
							System.out.println("Multiplication  of two number : "+Mul);
						}
						
						break;
						//(/ and Div) stands for division of 2 number 
					case '/':
						{
							double Div=first_no/second_no;
							System.out.println("Division  of two number : "+Div);
						}
						
						break;
						//(% and mod) stands for module of 2 number 
					case '%':
					{
						double  mod=first_no%second_no;
						System.out.println("Module  of two number : "+mod);
					}
					
					break;

					default:
						break;
					}
				
				break;
				
				
			default:
				System.out.println("You have made a Wrong Choice....Re-enter The No");
				break;
				
				
			}
			
			//if we type yes then we can perform next perform
			
			System.out.println("Do you want to continue Y/N");
			ans=sc.next().charAt(0);
		}
		while(ans=='y'||ans=='Y');
		
			
					
	}

}




