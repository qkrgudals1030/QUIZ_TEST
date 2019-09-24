1. C언어의 특징과 장점을 적으시오.

C언어는 실행속도가 빠르며 함수기반 언어로 프로그램의 구조화가 쉽다. 하드웨어를 제어하기 쉽고, 포인터 메모리에 직접 접근할 수 있다. 시스템 간의 호환 및
이식성이 좋다.

2. C언어의 활용에 대해 적으시오. 

스마트폰을 포함한 임베디드 프로그램에 많이 활용된다.

3. 두 실수를 메모리에 초기화하고 더하고 화면에 출력하시오.

#include<stdio.h>
int main(){
float a=2;
float b=3;
float c=a+b;
printf("%f", c);
}

4. 두실수를 키보드로 받고 더해서 화면에 출력하시오.

#include<stdio.h>
int main(){
float a, b, c;
printf("두수를 입력하시오.")
scanf("%f%f", &a, &b);
c=a+b;
printf("%f",c);
}

5. 두 실수를 메모리에 저장하고 함수 add()를 활용하여 더한 결과를 리턴 받아 화면에 출력하시오.

#include<stdio.h>
int add(float a,float b){
float c;
c=a+b;
return c;
}
void main(){
float s;
s = add(3,4);
printf("%f", s);
}

6. my.txt에 33과 22가 들어있다. 이를 읽고 더하고 결과를 출력하시오.

#include<stdio.h>
int main(){
int x,y;
FILE*fp;
fp=fopen("c:\\USERS\\박형민\\Desktop\\my.txt","r");
fscanf(fp,"%d%d", &x, &y);
fclose(fp);
printf("%d", x+y);
}

7. 3개의 과일을 {"banana","orange","kiwi"} 초기화 하고 화면에 출력하시오.

#include<stdio.h>

int main(){
int i;
const char; c[3] ={"apple","kiwi","banana"};
for(i=0;i<3;i++)
printf("%s\n", c[i]);
}

8. 곱셉용 명령창 계산기를 구현하시오. 매개변수가 2개 이하면 프로그램이 종료된다.

#include<stdlib.h>
int main(int n, char* v[]) {
int a, b, c;
printf("%d\n", n);
if (n < 4) {
printf("매개변수가 모자라요.\n");
exit(0);
}
a = atoi(v[1]);
b = atoi(v[3]);
switch (v[2][0]) {
case '*': c = a * b; break;
default: break;
}
printf("%d\n", c);
}

9. 두 명의 {이름,나이,이메일}을 구조체 배열에 초기화하고 화면에 출력하시오.

#include<stdio.h>
struct user{
int age;
char n[80];
char e[80];
int main(){
int i;
struct user we[2] ={{20,"phm","123@naver.com"},{19,"psb","234@naver.com"}};
printf("%d %s %s\n", we[0].age, we[0].n, we[0].e);
printf("%d %s %s\n", we[1].age, we[1].n, we[1].e);
}


10. 두 명의 {이름과 나이 그리고 이베일}을 구조체 배열에 초기화하고, 함수 pr()에 포인터 전달하고 화면에 출력 하시오.

include<stdio.h>
struct user{
int age;
char n[80];
char e[80];
};
void pr(struct user *we){
printf("%d %s %s\n", we->age, we->n, we->e);
we++;
printf("%d %s %s\n", we->age, we->n, we->e);
int main(){
struct user we[2] ={{20, "phm","123@naver.com"},{19."psb","234@naver.com"}};
pr(we);
}
