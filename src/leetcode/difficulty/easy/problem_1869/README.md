# 1869. Longer Contiguous Segments of Ones than Zeros
이진 문자열 `s`가 주어진다.  
가장 긴 연속된 `1`의 부분 문자열과 `0`의 부분 문자열이 있을 때  
`1`의 경우가 `0`보다 크면 `true` 그 외의 경우 `false`를 반환한다.  
- 예를 들어 `s = "110100010"`이라면 `1`의 경우 2, `0`의 경우 3이 가장 긴 연속된 부분 문자열의 길이다.
- 만약 세그먼트 자체가 없다면 가장 긴 연속된 부분 문자열의 길이는 `0`으로 간주한다.
### 입력제한
- 1 <= `s.length()` <= 100
- `s[i]`는 `'0'` 또는 `'1'`로 구성된다.
### 풀이핵심
- 각 세그먼트 별로 연속되는 세그먼트의 가장 긴 길이를 구한 후 둘을 비교해 `true` 또는 `false`를 반환한다.
### 문제풀이
1. 아래의 변수를 생성하고 초기화한다.
   - `count` : 연속된 세그먼트의 길이를 저장, 초기값 `0`
   - `maxZero` : `0` 세그먼트의 가장 긴 연속 부분 문자열의 길이를 저장, 초기값 `0`
   - `maxOne` : `1` 세그먼트의 가장 긴 연속 부분 문자열의 길이를 저장, 초기값 `1`
   - `prev` : 연속이 끊겼을 때 이전에 연속되던 문자를 저장, 초기값 `' '`
2. 아래의 연산을 `s`의 길이만큼 반복한다.
   - `c`에 현재 인덱스의 `s`의 문자를 저장한다.
   - 만약 `prev`와 `c`가 다를 경우 아래의 연산을 수행함
     - `prev`를 `c`로 수정
     - 만약 `c`가 `1`이고 `maxZero`보다 `count`가 크면 `maxZero`를 `count`로 수정
     - 만약 `c`가 `0`이고 `maxOne`보다 `count`가 크면 `maxOne`을 `count`로 수정
     - `count`를 `1`로 초기화한 후 다음 반복으로 넘어간다.
   - 만약 `prev`와 `c` 같은 경우
     - `count`를 `1` 증가시킨다.
3. `(2)`과정을 마쳤다면 아직 남아있는 `count`에 대한 값을 처리한다.
   - `prev`가 `0`이고 `maxZero`보다 `count`가 크면 `maxZero`를 `count`로 수정
   - `prev`가 `1`이고 `maxOne`보다 `count`가 크면 `maxOne`을 `count`로 수정
4. `maxZero < maxOne`의 결과를 반환한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/longer-contiguous-segments-of-ones-than-zeros/)
### 태그
`연속된 세그먼트의 부분 문자열 길이 비교`