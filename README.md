#### C语言不能按引用传值，但C++可以

下面是按引用求一组数的最大值，最小值，平均值，c++类型的文件才能正常运行
```c
#include<stdio.h>
void calculateMax(int &a,int &b,int &c,int &d,int &Max);
void calculateMin(int &a,int &b,int &c,int &d,int &Min);
void calculateAvg(int &a,int &b,int &c,int &d,double&Avg);
int main()
{
	int a,b,c,d;
	int Max,Min;
	double Avg;
	scanf("%d%d%d%d",&a,&b,&c,&d);
	calculateMax(a,b,c,d,Max);
	calculateMin(a,b,c,d,Min);
	calculateAvg(a,b,c,d,Avg);
	printf("最大值:%d\n",Max);
	printf("最小值:%d\n",Min);
	printf("平均值:%lf\n",Avg);
	return 0;
}
void calculateMax(int &a,int &b,int &c,int &d,int &Max)
{
	int p=a;
	if(p<a) p=a;
	if(p<c) p=c;
	if(p<d) p=d;
	Max=p;
}
void calculateMin(int &a,int &b,int &c,int &d,int &Min)
{
	int p = a;
	if(p>b) p=b;
	if(p>c) p=c;
	if(p>d) p=d;
	Min = p;
}
void calculateAvg(int &a,int &b,int &c,int &d,double &Avg)
{
	Avg=(a+b+c+d)/4.0;
}

```
