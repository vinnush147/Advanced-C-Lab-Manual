### EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:
```c
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    if (n >= 21 && n <= 29) {
        switch (n) { 
            case 21: printf("twenty one\n"); break;
            case 22: printf("twenty two\n"); break;
            case 23: printf("twenty three\n"); break;
            case 24: printf("twenty four\n"); break;
            case 25: printf("twenty five\n"); break;
            case 26: printf("twenty six\n"); break;
            case 27: printf("twenty seven\n"); break;
            case 28: printf("twenty eight\n"); break;
            case 29: printf("twenty nine\n"); break;
        }
    } else if (n > 29) {
        printf("Greater than 29\n");
    }

    return 0;
}


```

Output:
<img width="265" height="146" alt="8(1)" src="https://github.com/user-attachments/assets/1b85e584-a62a-4e09-adc4-4b2451ed7925" />



Result:
Thus, the program is verified successfully
 
### EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```c
#include <stdio.h>
#include <string.h>
int main() {
    char str[1001];  
    int freq[10] = {0}; 
    scanf("%s", str);
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= '0' && str[i] <= '9') {
            freq[str[i] - '0']++; 
        }
    }
    for (int i = 0; i < 10; i++) {
        printf("%d ", freq[i]);
    }
    printf("\n");
    return 0;
}

```

Output:
<img width="370" height="220" alt="8(2)" src="https://github.com/user-attachments/assets/51c8aeb1-ef67-4c35-90ee-1c2317cf61ed" />

Result:
Thus, the program is verified successfully

### EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```c
# include <stdio.h>
# include <string.h>
# include <stdbool.h>
void swap(char *a,char *b)
{
    char temp[100];
    strcpy(temp,a);
    strcpy(a,b);
    strcpy(b,temp);
}
bool permutation(char a[][100],int n)
{
    int k = -1;
    int l;
    for(int i=0;i<n-1;i++)
    {
        if(strcmp(a[i],a[i+1]) <0)
        {
            k = i;
        }
    }
    if(k==-1)
    {
        return false;
    }
    for(int i=k+1;i<n;i++)
    {
        if(strcmp(a[k],a[i]) < 0)
        {
            l = i;
        }
    }
    swap(a[k],a[l]);
    
    for(int i=k+1,j=n-1;i<j;i++,j--)
    {
        swap(a[i],a[j]);
    }
    return true;
}
int main()
{
    int n;
    scanf("%d",&n);
    char a[n][100];
    for(int i=0;i<n;i++)
    {
        scanf("%s",a[i]);
    }
    
    do{
        for(int i=0;i<n;i++)
        {
            printf("%s ",a[i]);
        }
        printf("\n");
    }while(permutation(a,n));
    
}


```

Output:

<img width="427" height="303" alt="8(3)" src="https://github.com/user-attachments/assets/94b361a5-39bf-494c-b1d6-d7d1ecd06546" />


Result:
Thus, the program is verified successfully
 
### EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:
```c
#include<stdio.h>
int main()
{
    int n,s=0;
    scanf("%d",&n);
    int l=2*n-1;
    int e=l-1;
    int a[l][l];
    while(n!=0)
    {
        for(int i=s;i<=e;i++)
        {
            for(int j=s;j<=e;j++)
            {
                if(i==s || i==e || j==s|| j==e){
                    a[i][j]=n;
                }
            }
        }
        s++;
        e--;
        n--;
    }
    for(int i=0;i<l;i++)
    {
        for(int j=0;j<l;j++)
        {
            printf("%d ",a[i][j]);
        }
        printf("\n");
    }
}
```

Output:


<img width="382" height="432" alt="8(4)" src="https://github.com/user-attachments/assets/50758925-96d3-4abf-83a1-bd67d2af5dfe" />

Result:
Thus, the program is verified successfully

### EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
 o	Declare an integer variable to store the number.
 o	Ask the user to input a number.
 o	Calculate the square of the number (multiply the number by itself).
 o	Return the squared value.
4.	In the main function:
 o	Call the square() function and display the result.
5.	End.

Program:
```c
#include<stdio.h>
int main()
{
    int n,sum=0;
    scanf("%d",&n);
    int a[n];
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
        sum+=a[i];
    }
    printf("%d",sum);
}


```

Output:

<img width="485" height="287" alt="8(5)" src="https://github.com/user-attachments/assets/54ce4f95-57c2-4978-ae37-2bc582a558d5" />

Result:
Thus, the program is verified successfully



























