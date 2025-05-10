# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>
int main(){
    float a,b;
    scanf("%f %f",&a,&b);
    float *p1=&a;
    float *p2=&b;
    float formula=0.5*(*p1)*(*p2);
    printf("area of the triangle with base %.6f and height%.6f=%.6f",*p1,*p2,formula);
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/a0b5c173-7edc-49a1-9655-8db621c7bcb1)

		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'C PROGRAM' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char *text = (char *)malloc(10 * sizeof(char));
    strcpy(text, "C PROGRAM");
    printf("%s\n", text);
    free(text);

    return 0;
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/ff79ceee-9400-4d49-8c8d-00690bac9b9d)




## RESULT
Thus the program to print 'C PROGRAM' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, gender,age and address as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <string.h>
 
struct student 
{
            char name[20];
            char gender[20];
            int age;
            char address[20];
};
 
void func(struct student record);
 
int main() 
{
            struct student record;
            scanf("%s %s %d %s",record.name,record.gender,&record.age,record.address);
 
            func(record);
            return 0;
}
 
void func(struct student record)
{
           printf("Name is: %s\n",record.name);
            printf("Gender: %s\n",record.gender);
             printf("Age is: %d\n",record.age);
             printf("Address: %s",record.address);
}
```


## OUTPUT
![image](https://github.com/user-attachments/assets/495cb71d-76b4-4199-8ef5-6f348ce2bc33)


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
int main()
{
    int empno[3];
    char dept[3][20];
    int basic[3];
for(int i=0; i<3; i++)
    {
     scanf("%d %s %d", &empno[i],dept[i], &basic[i]);
    }
printf("Details of the Employee: \n");
for(int i=0; i<3; i++)
    {
       float da=0.10f*basic[i];
       float hra=0.30f*basic[i];
      float gross=basic[i]+da+hra;

  printf("%d %s %d %.0f %.0f %.2f\n",empno[i], dept[i], basic[i],da,hra,gross);
}
    return 0;
}

```

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/6ee8ef15-98e5-4f94-b85a-cb0b87b2c7f0)


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -EB BILL CALCULATION USING STRUCURE

## AIM
Create a structure for eb calculation bill for 3 Customers(use customer no,prev reading & curre reading as input) using nested structure ( first 100 unit 2 Rs per unit ,101 to 200 rs.3 per unit and above 200 rs 5 per unit)

.

## ALGORITHM 
1. Start the program.

2. Define a structure e_bill containing:

3. Integer no (customer number)

4. Nested structure reading with integers p (previous) and c (current)

5. Float price (bill amount)

6. Declare an array of e_bill structures to hold details for 3 customers.

7. Input loop (repeat for 3 customers):

8. Read customer number, previous reading, and current reading using scanf.

9. Processing loop:

Calculate unit = current - previous.

If unit <= 100: price = unit * 2.0

If unit > 100 and <= 200: price = 100 * 2.0 + (unit - 100) * 3.0

If unit > 200: price = 100 * 2.0 + 100 * 3.0 + (unit - 200) * 5.0

10. Output loop:

11. Print customer number and corresponding bill using printf.

12. End the program.

## PROGRAM
```
#include<stdio.h>
struct e_bill{
    int no;
    struct reading{
        int p;
        int c;
    }r;
    float price;
};
int main(){
    int i;
    struct e_bill a[100];
    for(i=0;i<3;i++){
        scanf("%d%d%d",&a[i].no,&a[i].r.p,&a[i].r.c);
    }
    for(i=0;i<3;i++){
        int unit=a[i].r.c-a[i].r.p;
        if(unit<=100){
            a[i].price=unit*2.0;
        }
        else if(unit>100&&unit<=200){
            a[i].price=100*2.0+(unit-100)*3.0;
        }
        else{
            a[i].price=100*2.0+100*3+(unit-200)*5.0;
        }
    }
    printf("Details of the EB Customer\n");
    for(i=0;i<3;i++){
        printf("%d      %.2f\n",a[i].no,a[i].price);
}
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/a31f5b66-003a-43b4-afcb-a7d4eabe3c16)


 

## RESULT

Thus the C program to calculate eb bill calculation using nested structure has been executed successfully.
	


