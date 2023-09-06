# Checking-for-Prime-Number-using-Recursion-in-C

Checking for Prime Number using Recursion
Given a Number input num, write a program for Checking for Prime Number using Recursion in C Language.

For instance,

Input : num = 11
Output : Yes
Checking for Prime using Recursion in C
Checking for Prime Number Using Recursion In C
The objective of the code is to recursively check if the input number has more than 2 factors or not i.e 1 and the number itself. If it has more than two factors, the number is not a prime or it’s a prime otherwise. To do so we declare a recursive function and pass on the iteration value to check for factors and the number itself. As C can’t have Boolean functions return boolean datatype, we return 1 or 0. If the returned values is 1, then it’s true but if it’s 0 then it’s false. We set the base case as the iter value is equal to the number and when that is reaches we return 1 i.e it’s a Prime. We return the Recursive step call where we increment the iter value by 1 until the base case is satisfied. 

Lets try and understand the problem better using an example. Let the number be 5. As shown in the figure adjacent, the first call with  iter value as 2 because we know 1 is the common factor for all numbers. Now we check if iter value is equal to the number that is 5. If not we’ll try and check if the remainder of num/iter is 0 i.e num%iter == 0. If true we return 0 and terminate the recursion printing it’s not a prime. Else we keep going. We again increment the iter value to 3 as shown in the figure and check if 3 is a factor of 5. We keep checking recursively until the base case is satisfied when the iter is equal to the num at 5. We return the integer 1 and print that it’s a Prime Number.

Checking for Prime using Recursion in C
While loop in C
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Smallest element in an array

Power of a Number

Largest element in an array

C Code
Run
#include 
#include 

int CheckPrime(int i,int num)
{
    if(num==i)
        return 0;
    else
        if(num%i==0)
            return 1;
    else{
        return CheckPrime(i+1,num);
    }
}
int main()
{
    int num = 11;
    
    if(CheckPrime(2,num)==0)
        printf("It is a Prime Number.");
    else
        printf("It is not a Prime Number.");
}
Output
It is a Prime Number.
Explanation

The objective of the above code is to recursively increment the value of the check variable i which is initially set to 2. with each recursive step call the value of i goes up by 1. The recursion goes on until the base case is satisfied.

The algorithm for the above code is as follows,

Include the required libraries using include keyword.
Define a function CheckPrime() which accepts the check variable i and the number to be checked num and returns an integer value.
Set the base case as num == i and increment the check variable value by 1 with each recursive step call and return the output.
In int main() function, initialize all the required variables and call the function in an if statement such that if the returned value is 1, Print “It’s a Prime”. Print “It’s not a prime” otherwise.
The output for the code above is “It is a Prime Number.” if true and “It is not a Prime Number.” otherwise.
