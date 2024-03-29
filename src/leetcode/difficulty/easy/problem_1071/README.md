# 1071. Greatest Common Divisor of Strings
두 개의 문자열 `s`와 `t`가 있을 때, `s = t + t + ... + t`일 경우 `"t가 s를 나눈다"`라 할 수 있다.  
(즉, `t`가 한 번 이상 연결된 경우)  

문자열 `str1`과 `str2`가 주어질 때, 두 문자열을 나누는 가장 긴 문자열 `x`를 반환한다.
### 입력제한
- 1 <= `str1.length(), str2.length()` <= 1000
- `str1`과 `str2`은 `영대문자`로 구성된다.
### 풀이핵심
- 문자열 자체를 비교하기 보다 문자열 길이에 초점을 맞춘다.
  - 가장 긴 `x`를 구하기 위해선 `최대 공약수`를 구해야하기 때문
- 만약 두 문자열이 같은 `x`로 나눠진다면 두 문자열의 순서를 바꿔 연결했을 때의 문자열이 같아야한다.
### 문제풀이
1. `str1 + str2`과 `str2 + str1`의 결과 문자열이 같다면 두 문자열은 같은 문자열 `x`로 나누어짐을 뜻한다.
    - 만약 두 결과 문자열이 서로 다르다면 `""`를 반환한다.
    - 같다면 `(2)`과정을 수행한다.
2. `str1, str2`의 길이를 각각 `length1, length2`에 저장한다.
    - 가장 긴 `x`를 구하기 위해 `xLength`를 생성해 `1`로 초기화한다.
    - `length1, lenght2`중 더 작은 값을 `minLength`에 저장한다.
      - `x`의 최대 길이는 결국 `minLength`보다 작거나 같기 때문
3. `i`에 인덱스가 아닌 길이 값을 저장해 `minLength`부터 `1`까지 아래의 연산을 반복한다.
    - `i`가 `length1, length2`의 공통 약수라면 `xLength`에 `i`를 저장하고 반복을 종료한다.
4. `str1(또는 str2)`에서 인덱스 `[0,xLength]`범위의 부분 문자열을 반환한다. 
### 문제출처
- [leetcode](https://leetcode.com/problems/greatest-common-divisor-of-strings/)
### 태그
`다시 한 번 풀어볼 문제` `최대 공약수`