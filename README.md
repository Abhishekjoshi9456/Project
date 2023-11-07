# Project
                                              // BANK MANAGEMENT

	
#include<iostream>
#include<stdio.h>
#include<conio.h>
using namespace std;
 
class bank_management
{
	char name[100],add[100],y;
	int balance;
	public:
		void open_account();
		void deposite_money();
	    void withdraw_money();
	    void display_account();
	    
 };
 void bank_management::open_account()
 {
 	cout<<"enter your full name : ";
 	cin.ignore();            // for clear buffer
 	cin.getline(name,100);   //for strings
 	cout <<"enter your address : ";
 	cin.ignore();
 	cin.getline(add,100); 
 	cout<<"what type of account you want to open saving (s) or currunt (c) : ";
 	cin>>y;
 	cout<<"enter your amount for diposite : ";
 	cin>>balance;
 	cout<< " your account is created \n";
  } 
void bank_management::deposite_money()
{
	int x;
	cout<<"enter how much you diposite : ";
	cin>>x;
	balance+=x;
	cout<<"total amount you diposite : \t"<<balance<<"\n";
}
void bank_management::display_account()
{
	cout<<"\nyour full name :\t"<<name;
	cout<<"\nyour address :\t"<<add;
	cout<<"\ntype of account that you open :\t"<<y;
	cout<<"\namount you diposite :\t"<<balance<<"\n";
}
void bank_management::withdraw_money()
{
	float amount;
	cout<<"\n withdraw :";
	cout<<"enter amount to withdraw :";
	cin>>amount;
	balance = balance-amount;
	cout<<"now total amount is left :"<<balance<<"\n";
}
int main ()
{
	int n,a;
	bank_management obj;
  do
	{
	cout<<"1)  open account \n";
	cout<<"2)  deposite money \n";
	cout<<"3)  withdraw money \n";
	cout<<"4)  display account \n";
	cout<<"5)  exit \n";
	cout <<"select the option from above \n";
	cin>>n;
	switch(n)
	{
		  case 1:
		  cout<<"1) open account \n";
		  obj.open_account();
		  break;
		  case 2:
		  cout<<"2) diposite money \n";
		  obj.deposite_money();
		  break;
		  case 3:
		  cout<<"3) withdraw money \n";
		  obj.withdraw_money();
		  break;
		  case 4:
		  cout<<"4) display account \n";
		  obj.display_account();
		  break;
		  case 5:
		  	if (n==5)
		  	{
		  		exit(1);
			}
	default:
	     cout <<"this is not exist try again\n";
	}
	cout <<"do you want to select next option than press :: N \n";
	cout<<"if you want to exit than press :: E \n";
	a =getch();
	if (a=='e'||a=='E')
      	{
	    	exit(0);
      	}	
   }while (a=='n'||a=='N');
	getch();
	return 0;
}
