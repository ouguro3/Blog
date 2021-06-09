---
title: 평균
date: 2021-06-08 01:08:23
categories: 
 - algorithm
 - baek joon
---
**백준 알고리즘 1차원 배열 문제**
___
**세준이는 기말고사를 망쳤다 그래서 점수를 조작하기로 했다**  

**일단 자기 점수중 최댓값을 고르고 모든 점수를 점수/최대값 * 100으로 고쳤다**  

**바뀐 점수로 새로운 평균을 구하시오**

**입력**

___
**첫째줄에 시험 본 과목의 개수 N 이 주어진다  
둘째줄에 세준이의 현재 성적이 주어진다**

**출력**

___
**첫째 줄에 새로운 평균을 출력한다.**

```
# Ex 입력
3
40 80 60
```
```
# Ex 출력
75.0
```
```
# 작성 답안

# 수정 전

total = 0
n = int(input())
b = list(map(int,input().split()))
for i in range(n):
    b.sort()
    b[i] = b[i] / max(b) * 100
    print(b)
for i in b:
    total += i
total /= n
print(total)


# 수정 후
total = 0

n = int(input())
b = list(map(int,input().split()))
max_num = max(b)
for i in range(n):
    b[i] = b[i] / max_num * 100
for i in b:
    total += i
total /= n
print(total)
```

**막혔던점 : 40 80 60 입력을 받아 for문으로 새로운 평균을 구하는데  
60의 새로운 평균이 정상적으로 나오지 않았다**  

**원인 : `b[i] = b[i] / max(b) * 100`  코드에 max값을 실시간으로 가져오니  
바뀐 평균값에서 max값이 변경되어 60의 평균이 제대로 나오지 않았던것**  

**수정 : max_num 변수를 지정해 for문 외부에서 max값을 미리 저장해놨다  
그 후 동일한 코드에서 `max(b)` 부분에 `max_num` 을 대입 👍**