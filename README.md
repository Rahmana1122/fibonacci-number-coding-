# fibonacci-number-coding-
1000-digit fibonacci number for projects and What is the index of the first term in the Fibonacci sequence to contain 1000 digits?
   //     problem 25: 1000-Digit Fibonacci number
                        
						      //    Rahman ali
#include<iostream>
using namespace std;
int main()
{
	const int k =1000;
	int number[3][k]={0},carry,i,counter=2;
	number[2][k-1]=number[1][k-1]=1;
	while(number[0][0]==0){
		carry=0;
		for (i=k-1; i>=0; i--){
			number[0][i]=(number[1][i]+number[2][i] + carry)% 10;
			carry = (number[1][i]+number[2][i]+carry)/10;
			
		}
		for(i=k-1; i>=0; i--){
			number[2][i]= number[1][i];
			number[1][i]= number[0][i];
		}
		counter++;
	}
	cout<<"first term in the fibonacci sequence to contain 1000 digits is \n="<<counter<<endl;}
