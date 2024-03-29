# 2652. Sum Multiples
양의 정수 `n`이 주어질 때, `3` 또는 `5` 또는 `7`로 나눌 수 있는 정수를 `[1, n]` 범위에서 구해 모두 더한 값을 구한다.  
주어진 범위에서 제약 조건을 만족하는 모든 정수의 합을 반환한다.
### 입력제한
- 1 <= `n` <= 1000
### 풀이핵심
- 즉 `[1,n]`범위에서 `3, 5, 7`의 배수인 정수들을 구해 모두 더한다.
  - 단, 중복되는 경우(3의 배수이면서 5의 배수인 15)는 카운트하지 않는다.
  - 두 수의 배수이면 둘 중 하나의 배수로만 쳐야함.
### 문제풀이
1. 제약 조건으로 나올 수 있는 최소 배수는 3의 배수인 `3`이다.
    - `n`이 `3`미만이라면 제약 조건에 해당하는 정수는 없으므로 `0`을 반환한다.
2. `(1)`의 조건에 해당하지 않는 경우 `3`부터 `n`까지 아래의 연산을 반복한다.
   - `i`를 `3`으로 나눈 나머지가 `0`인 경우(3의 배수)
     - `result`에 `i`를 더해 저장하고 다음 반복을 수행한다.
   - `i`를 `5`으로 나눈 나머지가 `0`인 경우(5의 배수)
       - `result`에 `i`를 더해 저장하고 다음 반복을 수행한다.
   - `i`를 `7`으로 나눈 나머지가 `0`인 경우(7의 배수)
       - `result`에 `i`를 더해 저장하고 다음 반복을 수행한다.
3. `(2)`의 과정이 끝났다면 `result`를 반환한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/sum-multiples/)
### 태그
`정수의 배수`