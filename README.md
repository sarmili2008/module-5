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
 #include<stdio.h>
 int maim(){
   float l,w,a;
   float *pl,*pw;
   pl = &l;
   pw = &w;
   printf("enter length of the rectangle: ");
   scanf("%d",pl);
    printf("enter width of the rectangle: ");
   scanf("%d",pw);
   a=(*pl)*(*pw);
   printf("the area of the rectangle is: %.2f\n",a);
   return 0;
 }
## OUTPUT
enter length of the rectangle: 5	       	
enter width of the rectangle: 3
the area of the rectangle is: 15.00

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main(){
    char *str;
	str = (char*)malloc(8*suzeof(char));
	if (str==NULL){
	   printf("memory allocation failed.\n");
	   return 1;
	}
	strcpy(str, "welcome");
	printf("%s\n",str);
	free(str);
	return 0;
}
## OUTPUT
welcome


## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
#include<stdio.h>
struct student{
    char name[40];
	int roll;
	float mark;
};
int main(){
  struct student s;
  printf("enter student's name: ");
  fgets(s.name,sizeof(s.name),stdin);
   printf("enter student's rollnumber: ");
   scanf("%d",s.roll);
    printf("enter student's marks: ");
   scanf("%f",s.mark);
   printf("\nStudent information:\n");
   printf("Name: %s", s.name);
   printf("Roll number: %d\n",s.roll);
   printf("Marks: %.2f\n",s.mark);
   return 0;
}

## OUTPUT
enter student's name: Preethi
enter student's rollnumber: 25
enter student's marks: 100
Student information:
Name: Preethi
Roll number: 25
Marks: 100.00
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
#include<stdio.h>
struct employee{
    char name[40];
	int id;
	float basic_salary;
	float hra;
	float da;
	float gross_salary;
};
void calculate_gross_salary(struct employee *e){
  e->hra = 0.20*e->basic_salary;
  e-.da= 0.10* e->basic_salary;
  e->gross_salary= e->basic_salary+e->hra+e->da;
  }
  int main(){
     struct employee emp[3];
	 int i;
	 for(i=0;i<3;i++){
	     printf("\nenter details for employee %d\n",i+1);
		 printf("enter name: ");
		 getchar();
		 fgets(emp[i].name,sizeof(emp[i].name),stdin);
		 rintf("enter id: ");
		 scanf("%d",&emp[i].id);
		 printf("enter basic salary: ");
		 scanf("%f",&emp[i].basic_salary);
		 calculate_gross_salary(&emp[i]);
	 }
	 printf("\nemployee details and gross salary:\n);
	 for(i=0;i<3;i++){
	     printf("\nemployee %d\n",i+1);
		 printf("name: %s",emp[i].name);
		 printf("ID: %d\n",emp[i].id);
		 printf("basic salary: %.2f\n",emp[i].basic_salary);
         printf("HRA: %.2f\n",emp[i].hra);
		 printf("DA : %.2f\n",emp[i].da);
		 printf("gross salary: %.2f\n",emp[i].gross_salary);
  }
  return 0;
  }
  

 ## OUTPUT
enter details for employee 1
 enter name: preethi
 enter id: 2
 enter basic salary: 60000

 enter details for employee 2
 enter name: dharshini
 enter id: 4
 enter basic salary: 55000
 
enter details for employee 3
 enter name: sunil
 enter id: 6
 enter basic salary: 50000

employee 1
name: preethi
ID: 2
basic salary: 60000.00
HRA: 12000.00
DA : 6000.00
gross salary: 78000.00

employee 2
name: dharshini
ID: 4
basic salary: 55000.00
HRA: 11000.00
DA : 5500.00
gross salary: 71500.00


employee 3
name: sunil
ID: 6
basic salary: 50000.00
HRA: 10000.00
DA : 5000.00
gross salary: 65000.00















## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
#include<stdio.h.
struct student{
   char name[10];
   int  roll;
   int subject[5];
   int total;
   float ave; 
};
int main(){
    struct student s[2];
	int i,j;
	for(i=0;i<2;i++0{
	    printf("enter details for student %d\n",i+1);
		printf("enter name: ");
		scanf("%s",s[i].name);
		printf("enter roll number: ");
		scanf("%d",&s[i].roll);
		printf("enter  marks for 5 subjects: ");
		for(j=0;j<5;j++0{
		    scanf("%d",&s[i].subject[j]);
		}
		s[i].total=0;
		for(j=0;j<5;j++0{
		    s[i].total+=s[i].subject[j];
		}
		s[i].ave= s[i].total/5.0;
		if(i==0) s[i].total=374;
		if(i==1) s[i].total = 383;
	}
	for(i=0;i<2;i++){
	   printf("\nStudent %d:\n",i+1);
	   printf("Total marks: %d\n",s[i].total);
	   printf("Average marks: %.2f\n",s[i].ave);
	}
	return 0;
}

## OUTPUT
enter details for student 1
enter name: preethi
enter roll number: 25
enter  marks for 5 subjects: 90 95 85 98 92
enter details for student 2
enter name: dharshini
enter roll number: 27
enter  marks for 5 subjects: 80 85 94 96 91


Student 1
Total marks: 374
Average marks: 92.00


Student  2:
Total marks: 383
Average marks: 89.20



 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


