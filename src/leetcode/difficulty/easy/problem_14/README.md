# 14. Longest Common Prefix
문자열 배열 `strs`에서 가장 긴 `공통 접두사(문자열)`를 찾는다.  
만약 공통 접두사가 없다면 `""(빈 문자열)`을 반환한다.
### 입력제한
- 1 <= `strs.length` <= 200
- 0 <= `strs[i].length()` <= 200
- `strs[i]`는 오직 `영소문자`로 구성된다.
### 풀이핵심
- `strs`의 요소 중 `""`이 있다면 공통 접두사를 가질 수 없다.
- `strs[i]`중에 `""`가 없다면 `strs[0]`의 문자를 가지고 나머지 요소의 문자와 비교한다.
### 문제풀이
1. 만약 `strList`가 `""`을 요소로 가진다면 `""`을 반환한다.
2. `(1)`의 조건에 부합하지 않는다면 아래의 연산을 반복한다.(반복 조건은 `strs[0]`을 기준으로한다.)
    - `strs[0]`의 인덱스 `i`에 위치한 문자를 `c`에 저장한다.
    - `checkPrefix()`의 결과가 `false`라면 반복을 종료한다.
      - `checkPrefix()` : `strList`와 `c`,`i`를 파라미터로 받아 모든 요소가 `c`를 `i`위치에 가지고 있는지 확인한다.
    - `true`라면 `prefix`에 `c`를 추가한다.
3. `(2)`의 과정이 끝났다면 `prefix`를 문자열로 형변환해 반환한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/longest-common-prefix/)
### 태그
`가장 긴 공통 접두사`