1.리스트
--------
>리스트의 종류와 설명:

 1. Singly Linked List
 
 노드안에 링크가 1개이고
 
 단방향으로 진행하는 리스트
 
 2. Doubly Linked List
 
 노드안에 링크가 2개이고 양방향으로 
 
 진행할수있는 리스트
 
 3. Circular Linked List
 
 마지막 노드가 첫번째 노드를 가르켜서
 
 계속 회전할수있게 만들어진 리스트
 
>리스트 예제 코드

#include <stdio.h>

#include <stdlib.h>

typedef struct list {

 int d;

 struct list* p;

} LIST;

LIST* root = NULL;

LIST* last = NULL;

void AddList(int a){

 LIST* r = (LIST*)malloc(sizeof(LIST));

 r->d = a;

 r->p = NULL;

 if(root==NULL) root = r;

 else           last->p = r;

 last = r;

}

int main(void){

 AddList(35);

 AddList(40);

 AddList(45);

 while(root){

  printf("%d\n", root->d);

  root = root->p;

 }

}
>3.그림설명
저는 쉽게 이해하기 위해 그림을 그려보았습니다.

***
2.트리
------
>트리의 종류와 설명
