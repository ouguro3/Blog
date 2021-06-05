---
title: 빠른 A + B
date: 2021-06-05 22:30:28
categories: 
 - algorithm
 - baek joon
---
**백준 알고리즘 for문 문제**

### 문제 1 : 빠른 A + B
___
입출력 방식이 느리면 여러 줄을 입력 받거나 출력할 때 시간초과가 날 수 있다  
그럴때는 sys.stdin.readline() 를 이용하면 된다  
단 이때 맨 끝의 개행문자 `\n` 까지 함께 입력되니 .rstrip() 을 써주는게 좋다  

  
입력  
___
첫 줄에 테스트케이스의 개수 T가 주어진다.
다음 T줄에는 각각 두 정수 A와 B가 주어진다.

출력
___
각 테스트케이스마다 A+B를 한 줄에 하나씩 순서대로 출력한다.

Ex 입력  
```
5
1 1
12 34
5 500
40 60
1000 1000
```
Ex 출력
```
2
46
505
100
2000
```
___
내 제출  
```
import sys # sys 모듈 불러오기
T = int(sys.stdin.readline().rstrip()) # 정수형으로 입력받고 맨 끝의 문자 삭제
num = []
for i in range(T): # 입력 받은 T 만큼 반복
    A,B = map(int,sys.stdin.readline().rstrip().split())
    C = A + B # 변수 C 에 A + B 의 값을 저장
    num.append(C) # num 빈 리스트에 C 의 값을 저장
for i in num:
    print(i)
```
이 문제를 풀면서 알게된것은 짧은 코드라면 차이가 없지만 매우 긴 코드를 작성 시  
input() 보다는 sys.stdin.readline() 의 속도가 압도적이라는것이다  

아직은 사용해볼 기회가 없었지만 미래에 쓰게될지 모르니 미리 습관을 들여놓는게  
좋을것같다  


