# Student-record-management--in-C    
It is a C program which stores any number of student's name and marks and displays them in new file "ct4exam.txt".    
The program uses file handling technique through which we can read a file or write them.It uses file handling functions.    
      
      
The code for above program is:-    
     
     
//Student record management system in c using file management     
#include<stdio.h>    
#include<stdlib.h>    
int main()    
{    
   char name[50];    
   int i,num;     
   float marks;     
   printf("please enter number of students ");     
   scanf("%d",&num);     
   FILE *fptr;     
   fptr=(fopen("C:\\ct4exam.txt","w"));    
   if(fptr==NULL)   
   {    
      printf("ERROR");    
      exit(1);    
   }    
   for(i=0;i<num;i++)    
   {     
      printf("For student %d\nEnter Name:",i+1);     
      scanf("%s",name);     
      printf("Enter marks");     
      scanf("%f",&marks);     
      fprintf(fptr,"\nName:%s\nMarks:%.2f\n",name,marks);     
   }      
}      
