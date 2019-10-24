:star: 下面就是有该错误的程序
```c
#include <stdio.h>
int main(void)
{
int dogs;
printf("How　many　dogs　do　you　have?\n");
scanf("%d",&dogs);
printf("So you have　%d　dog(s)!\n",　dogs);   --错误的原因就是，本行中有中文的空格，这个错误很难发现。
return　0;
}
```
