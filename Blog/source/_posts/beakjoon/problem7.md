---
title: OX 퀴즈
date: 2021-06-13 00:06:19
categories: 
 - algorithm
 - baek joon
---
**백준 알고리즘 1차원 배열 문제**
___
**OOXXOXXOOO 와 같은 OX퀴즈의 결과가 있다  
O는 문제를 맞은 것이고, X는 틀린것이다  
문제를 맞은 경우 그 문제의 점수는 연속된 O의 개수가 된다**

**ex) OOXXOXXOOO = 1+2+0+0+1+0+0+1+2+3 = 10**

**OX퀴즈의 결과가 주어졌을 때, 점수를 구하는 프로그램을 작성**  
___
**입력**

**첫째 줄에 테스트 케이스의 개수가 주어진다  
문자열은 O 와 X 로 이루어져있다**
```
2
OOXXOXXOOO
OOXXOOXXOO
```
___
**출력**  

**각 줄의 점수 출력**
```
10
9
```
___
**답안**
```
n = int(input())
for i in range(n):
    s = list(map(str,input()))
    count = 0
    total = 0
    for j in range(len(s)):
        if s[j] == 'O':
            count += 1
            total += count
        elif s[j] == 'X':
            count = 0
    print(total)

```
**처음에 count와 total을 초기화 하지않아 값이 엉뚱하게 나온것을 제외하면,**  

**별다른 어려움이 없었던 문제**  

**슬슬 문제가 복잡해지는것같다**
