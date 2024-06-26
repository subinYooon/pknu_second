# 이 코드는 집합 A가 주어졌을 때 관계 R이 동치 관계인지 판단하는 모듈이다.
## 함수 
### check_transitive(R) 
관계 R이 추이적임을 판단하는 함수
(a,b)와 (b,c)가 R에 존재하는지 판단한 후, b==c인지 확인

### check_symmetric(R) 
관계 R이 대칭 관계인지를 판단하는 함수
(a,b)와 (b,a)가 모두 R에 존재하는지 판단

### check_reflexive(R)
관계 R이 반사 관계인지를 판단하는 함수
(x,x)가 R에 포함되어있는지 판단

### check_equivalence(R, A) 
관계 R이 동치 관계인지 판단하는 함수
위 세 함수가 모두 True라면 동치관계 - True 반환
세 함수 중 하나라도 False - False 반환

### 사용 방법

#### 요소 집합 A와 관계 R을 정의한다
A = {1, 2, 3, 4}
R = {(1, 1), (1, 3), (2, 2), (3, 3), (3, 1), (3, 4), (4, 4), (4, 3)}

#### 속성을 검사한다
print("반사적:", check_reflexive(R, A))
print("대칭적:", check_symmetric(R))
print("추이적:", check_transitive(R))
print("동치 관계:", check_equivalence(R, A))
  
