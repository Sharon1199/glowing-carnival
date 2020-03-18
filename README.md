# glowing-carnival
Process Management Exercises
Code:

#include<stdio.h>
int main()
{
int pid;
pid=fork();
if(pid==0)
{
printf("this is child %d\n",pid);
}
else
{
printf("this is parent\n");
}

}

Code 2:

Add.c:

#include<stdio.h>
int main()
{
int sum=0,i;
for(i=1;i<5;i++)
{
sum=sum+i;
}
printf("addition of 5 nos%d",sum);
}

Execve.c:

#include<stdio.h>
int main()
{

int i= execve("/home/eg1/srihari/a.out",NULL,NULL);
}

Code 3:

#include<stdio.h>
int main()
{
int pid,status;
pid=fork();
if(pid<0)
{
printf("error");
}
else if(pid==0)
{
printf("child terminating\n");
exit(0);
}
if(wait(&status)!=pid)
printf("wait error\n");
else
printf("parent terminating\n");
}
