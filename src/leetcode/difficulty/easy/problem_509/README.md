# 509. Fibonacci Number
`피보나치 수열`은 일반적으로 `F(n)`으로 표기된다.  
각 수열은 `0`과 `1`에서 시작하며, 앞의 두 수열의 합이 된다.  
- `F(0) = 0` `F(1) = 1`
- `F(n) = F(n-1) + F(n-2)` (n > 1)

정수 `n`이 주어지면 `F(n)`을 반환한다.
### 입력제한
- 0 <= `n` <= 30
### 풀이핵심
- `피보나치 수열`을 활용해 `F(n)`을 구하면 된다.
### 문제풀이
1. `n`이 `1` 또는 `0`이라면 `n`을 반환
2. `(1)`의 경우가 아닐 경우
   - `fib(n-1)`과 `fib(n-2)`의 합을 반환한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/fibonacci-number/)
### 태그
`재귀 호출(함수)`