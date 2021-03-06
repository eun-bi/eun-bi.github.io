---
title:  "[Python] 리스트/튜플/딕셔너리/집합 자료형"
date:   2017-09-07 18:15
headerImage: false
layout: post
category: blog
tag: Python
author: eunbi
comments: true
---


리스트 / 튜플 / 딕셔너리 / 집합 자료형이 헷갈릴 때가 있어서 간단하게 개념 잡을 겸 정리해본다.



### **리스트(List) 자료형**


`리스트명 = [요소1, 요소2, 요소3 ...]`  
→ 어떠한 자료형이든 포함 가능

* **인덱싱과 슬라이싱**

```python
a = [1, 2, ['a', 'b', ['Life', 'is]]]
a[2][2][0] → 'Life'
```


* **삭제** : del 함수 사용  
```python
  del a[1]
```


* **리스트 관련 함수**
  - append(x) : 요소 x를 추가
  - sort : 정렬
  - reverse : 역순으로 뒤집기
  - index(x) : x의 위치값 반환
  - insert(a,b) : a번째 위치에 b를 삽입
  - remove(x) : x 삭제
  - pop : 마지막 요소를 반환하고 그 요소는 삭제
  - count(x) : x의 개수 반환
  - extend(x) :리스트 x를 더함



### **튜플(Tuple) 자료형**  


`튜플명 = (요소1, 요소2, 요소3...)`  
*괄호 생략 가능  

→ 리스트와 비슷한 개념
 리스트는 값의 생성, 삭제, 수정이 가능하지만 튜플은 **값의 수정이 불가능**하다.  

**+** 단 1개의 요소만을 가질 때는 콤마를 반드시 붙여야 함

```Python
  t = (1,)
```  


### **딕셔너리(Dictionary) 자료형**  


`사전명 = { 키1:값1, 키2:값2, 키3:값3 ...}`  

  → 키 값은 고유해야 한다.  
순차적으로 해당 요소값을 구하지 않고 **key 값을 통해 값을 얻음**

```python
  dict = {1:'a', 'b':4}
```

* **딕셔너리 쌍 추가**  

   사전명[키] = 값

  ```Python
  dict['g'] = 33
  dict = {'g':33, 1:'a', 'b':4}
  ```

* **삭제** : del 사전명[키]  


* **key를 사용해 데이터 값 얻기** : 사전명[키]

* **딕셔너리 관련 함수**
   - keys : key 만 모은 리스트 반환
   - values : value 만 모은 리스트
   - items : key, value 쌍을 튜플로 반환
        ```Python
          dict.keys()
          dict.values()
          dict.items()
        ```
   - clear : key, value 쌍을 모두 지움
   - get : key로 value 를 얻음
   - in : 해당 키가 딕셔너리 안에 있으면 true / 없으면 false 반환
      ```Python
        1 in dict
      ```


### **집합(set) 자료형**  

`집합명 = set(요소)`  
 →  요소는 리스트나 문자열 가능  
    중복을 허용하지 않는다.  
    순서가 없다. → 인덱싱으로 값을 얻을 수 없음

```Python
s = set("hello")
s  → {'e', 'l', 'o', 'h}
```  
→ 인덱싱으로 접근할 시 리스트나 튜플로 변환 후 가능

* 교집합 : & 또는 intersection 함수 사용
* 합집합 : | 또는 union 함수 사용
* 차집합 : - 또는 difference 함수 사용

* 집합 관련 함수
   - add(요소) : 값 1개 추가
   - update(요소1, 요소2...) : 값 여러 개 추가
   - remove(요소) : 요소 제거




---
기존 포스팅에서 옮겨옴  
(<https://blog.naver.com/uko02111/221091688359>)
