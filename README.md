# C_2-solo

1.
#include<stdio.h>


#include<stdlib.h>


int main(int n, char* v[]) {


int a, b, c;


if (n < 4) {


printf("매개변수가 모자라요.\n");


exit(0);


}


a = atoi(v[1]);

b = atoi(v[3]);


switch (v[2][0]) {

case '+': c = a + b; break;

case '-': c = a - b; break;

default: break;

}

printf("%d\n", c);

}


2.

#include<stdio.h>

#include<stdlib.h>

int add(int a, int b) {

return a + b;

}

int main() {

int a, b;

FILE* fp = fopen("my.txt", "r");

if (fp == NULL) { 

puts("File not found!!");

exit(0); 

}

fscanf(fp, "%d%d", &a, &b);

fclose(fp);

printf("%d\n", add(a, b));

}

(전처리기 정의에 들어가서;_CRT_SECURE_NO_WARNINGS 붙여준다)



3.세명의 구조체 정보(나이,이름,전화번호)를 배열에 초기화하고

포인터로 화면에 출력하시오.

#include<stdio.h>

struct user {

int a;

char n[80];

char m[80];

} we[3] = { { 18,"jjjunem",010-4584-8954 },{ 16,"kimt",010 - 4584 - 8954 }

,{ 19,"jum",010 - 4784 - 8554 } };

int main() {

struct user* p;

p = we;

printf("%d %s\n", p->a, p->n,p->m);

p++;

printf("%d %s\n", p->a, p->n, p->m);

p++;

printf("%d %s\n", p->a, p->n, p->m);

}


4.

#include<stdio.h>

struct user {

int a;

char n[80];

} we[2] = { { 18,"jcshim" },{ 16,"jskim" } };

int main() {

struct user* p;

p = we;

printf("%d %s\n", p->a, p->n);

p++;

printf("%d %s\n", p->a, p->n);

}



