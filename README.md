Given an integer N, write a program to count the number of twin prime pairs that exist in the range [1, N] (inclusive).

A twin prime pair is defined as two prime numbers (p, q) where:

p and q are both prime numbers.
q = p + 2, i.e., the two primes differ by exactly 2.
(p, q) and (q, p) should be counted as the same pair, so you should only count one of them.
Input Format

A single integer N
Constraints

1 ≤ N ≤ 10^6
Output Format

A single integer representing the count of unique twin prime pairs in the range [1, N].
Sample Input 0

10
Sample Output 0

2
Sample Input 1

20
Sample Output 1

4







#include<stdio.h>
int prime(int num) {
   for(int i=2; i*i<=num; i++){
        if(num%i==0)
            return 0;
    }
    return 1;
}

int main()
{
    int N;
    int count=0;
    scanf("%d",&N);

    for(int i=2; i<=N; i++)
    {
        if(prime(i)==1 && prime(i+2)==1)
            count++;
    }
    printf("%d",count);
    return 0;

}

