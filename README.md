#include
#include
void main()
{
int dd,mm,yy,ndd,dn,yr,rs,i,x,y,z,w,u,td,k,j,tm=0;
int mnth[12]={3,0,3,2,3,2,3,3,2,3,2,3};
char c;
clrscr();
do
{
printf(“\n Enter the any Date(dd/mm/yyyy):”);
scanf(“%d/%d/%d”,&dd,&mm,&yy);
if(yy30200)
printf(“\n :INVALID DATE:”);
else
{
if(mm12)
printf(“\n :INVALID DATE:”);
else
{
if(mm==1||mm==3||mm==5||mm==7||mm==8||mm==10||mm==12)
if(dd31)
printf(“\n INVALID DATE:”);
else
goto agn;
else if(mm==4||mm==6||mm==9||mm==11)
if(dd30)
printf(“\n INVALID DATE:”);
else
goto agn;
else if(mm==2 && (yy%400==0||(yy%100!=0 && yy%4==0)))
if(dd29)
printf(“\n INVALID DATE:”);
else
goto agn;
else if(mm==2 && !(yy%400==0 || (yy%100!=0 && yy%4==0)))
if(dd28)
printf(“\n INVALID DATE:”);
else
goto agn;

else
{

agn:
yr=yy-1;

ndd=01;
if(yy%400==0||(yy%100!=0 && yy%4==0))
{
mnth[1]=1;
}
else
mnth[1]=0;
tm=0;
for(i=0;i<=mm-2;i++)
tm=tm+mnth[i];
x=yr%400;
y=x/100;
z=x%100;
w=z/4;
u=z%4;

td=y*5+w*5+u;
rs=(td+tm+ndd)%7;
printf("\n");
printf("\t**This Software Is Developed By: VIKAS TIWARI**\n\n");
if(mm==1)
printf("\t\tJanuary\t%d\n",yy);
if(mm==2)
printf("\t\tFebuary\t%d\n",yy);
if(mm==3)
printf("\t\tMarch\t%d\n",yy);
if(mm==4)
printf("\t\tApril\t%d\n",yy);
if(mm==5)
printf("\t\tMay\t%d\n",yy);
if(mm==6)
printf("\t\tJune\t%d\n",yy);
if(mm==7)
printf("\t\tJuly\t%d\n",yy);
if(mm==8)
printf("\t\tAugust\t%d\n",yy);
if(mm==9)
printf("\t\tSeptember\t%d\n",yy);
if(mm==10)
printf("\t\tOctoober\t%d\n",yy);
if(mm==11)
printf("\t\tNovember\t%d\n",yy);
if(mm==12)
printf("\t\tDecember\t%d\n",yy);
printf("\n Mon \tTue \tWed \tThu \tFri \tSat \tSun\n");

if(mm==1||mm==3||mm==5||mm==7||mm==8||mm==10||mm==12)
dn=31;
if(mm==4||mm==6||mm==9||mm==11)
dn=30;
if(mm==2 && (yy%400==0||(yy%100!=0 && yy%4==0)))
dn=29;
if(mm==2 && !(yy%400==0||(yy%100!=0 && yy%4==0)))
dn=28;

if(rs==0)
{
printf("\t\t\t\t\t\t");
j=6;
}
if(rs==1)
{
j=0;
}
if(rs==2)
{
printf("\t");
j=8;
}
if(rs==3)
{
printf("\t\t");
j=9;
}
if(rs==4)
{
printf("\t\t\t");
j=10;
}
if(rs==5)
{
printf("\t\t\t\t");
j=11;
}
if(rs==6)
{
printf("\t\t\t\t\t");
j=12;
}
for(k=1;k30200)
yy=30200;
goto agn;
}
if(c==80)
{ clrscr();
yy=yy-1;

if(yy<1)
yy=1;
goto agn;
}
if(c==75)
{ clrscr();
–mm;
if(mm<1)
{
mm=12;
yy=yy-1;
if(yy12)
{
mm=1;
yy++;
if(yy>30200)
yy=30200;
}
goto agn;

}

}
}
} /*First else statemen */

printf(“\n Do You Want to Continue…..(y/n):”);
fflush(stdin);
c=getche();

}
while(c==’y’ || c==’Y’);

getch();
}
