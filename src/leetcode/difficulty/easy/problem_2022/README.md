# 2022. Convert 1D Array Into 2D Array
1차원 정수 배열 `original`과 두 개의 정수 `m, n`이 주어진다.  
`original`의 모든 요소를 사용하여 행과 열이 `m` `n`인 2차원 배열을 생성한다.  
- `original`의 모든 요소를 순차적으로 2차원 배열에 저장해 구성한다.
  - 첫 번째 행에 요소를 채웠다면 다음 요소는 다음 행에 저장한다.

만약 2차원 배열로 구성할 수 있다면 생성한 `2차원 배열`을 반환  
구성할 수 없다면 `빈(길이 0) 배열`을 반환한다.
### 입력제한
- 1 <= `original.length` <= 5 * 10⁴
- 1 <= `original[i]` <= 10<sup>5</sup>
- 1 <= `m, n` <= 4 * 10⁴
### 풀이핵심
- 주어진 1차원 배열이 2차원 배열로 수정이 가능한지 확인이 필요함
### 문제풀이
1. `original`의 길이가 `m * n`과 다르다면 `빈 배열(길이가 0)`을 반환한다.
2. `reformat`을 생성하고 `행`과 `열`, `original`의 인덱스 변수를 생성하고 `0`으로 초기화한다.
3. `i`가 `ol`과 같아질 때까지 아래의 연산을 반복한다.
   - `original`의 요소를 `reformat`에 저장하고 `row`의 값을 `1`증가시킨다.
   - 만약 `row`가 `n`과 같아지면 `line`을 `1`증가시키고 `row`에 `0`을 저장한다.
   - `i`의 값을 `1` 증가시킨다.
4. `(3)`의 과정이 끝났다면 `reformat`을 반환한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/convert-1d-array-into-2d-array/)
### 태그
`[배열 -> 2차원 배열] 변환`