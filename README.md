appending-the-file

#include<stdio.h>
#include<conio.h>
#include<process.h>


void main()
{
clrscr();
FILE *fp;
char c=' ';
fp=fopen("shan.txt","r");
while(!feof(fp))
 {
 c=fgetc(fp);
 printf("%c",c);
 }
fp=fopen("shan.txt","a");
if(fp==NULL)
{
printf("enter a valid entry");
exit(1);
}
printf("enter the content to append");

while(c!='.')
{
c=getche();
fputc(c,fp);
}
fclose(fp);
printf("after the file");
fp=fopen("shan.txt","r");
while(!feof(fp))
{
c=fgetc(fp);
printf("%c",c);
}
getch();
}