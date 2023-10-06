# OS-EX.6-IMPLEMENTATION-OF-INTER-PROCESS-COMMUNICATION-USING-PIPE

## AIM:
To implement interprocess communication using pipe command.

## ALGORITHM:
1. Start
2. Create a child and parent using fork()
3. Allow communication between both the process
4. Stop

## PROGRAM:
`
#include<stdio.h>
main()
{
int p[2],pid,pid1;
char msg[25],msg1[25];
pipe(p);
pid=fork();
if(pid!=0)
{
sleep(2);
read(p[0],msg1,21);
printf(“%s”,msg1);
}
else
{
pid1=fork();
if(pid1!=0);
{
sleep(1);
read(p[0],msg1,21);
write(p[1],”Grand child says hello”,21);
}
else
write(p[1],”Says hello to grandpa”,29);
}
}
`

## OUTPUT:


## RESULT:
