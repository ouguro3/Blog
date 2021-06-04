---
title: 사분면 고르기
date: 2021-06-04 15:30:38
categories: algorithm
            - baek joon
---
**백준 알고리즘 if문 문제 1**

### 문제 1 : 사분면 고르기  
___
사분면은 아래 그림처럼 1부터 4까지 번호를 갖는다  

![사분면](https://user-images.githubusercontent.com/84296244/120756484-4329d980-c54a-11eb-8c40-8ddec8654746.PNG)

점의 좌표를 입력받아 그 점이 어느 사분면에 속하는지 알아내는 프로그램을 작성

입력  
___
첫 줄에는 정수 x 가 주어진다
다음 줄에는 정수 y 가 주어진다  

출력  
___
점 (x,y) 의 사분면 번호 (1,2,3,4 중 하나)를 출력한다


Ex 입력                                                     
```                                    
12
5
```
Ex 출력
```
1
```
___
내 제출
```
a = int(input()) # 정수 a 입력 
b = int(input()) # 정수 b 입력 
if a > 0 and b > 0:
    print('1')
elif a < 0 and b > 0:
    print('2')
elif a < 0 and b < 0:
    print('3')
else:
    print('4')
```

간단한 if 문 문제

두개의 정수를 입력받아 그 정수가 양인지 음인지 판별하면 되는 문제였다  

다만 여기에서는 사분면이라는 4개의 예가 있으므로 각 면에 해당하는 조건을  

and 연산자를 이용해 판별하였다  
___
[해당 코드의 깃허브](https://github.com/ouguro3/Study/blob/main/Baekjoon/if/01_if.py)  