# 2094. Finding 3-Digit Even Numbers
각 요소가 숫자인 정수형 배열 `digits`가 주어진다.  
해당 배열은 같은 값을 가진 요소를 중복으로 가질 수가 있다.  
아래의 요구사항을 충족하는 세 자리 정수들을 구해 정수형 배열로 반환한다.  

- 요소들을 한 번씩 사용해 세자리 정수를 만든다.
- 정수의 첫째자리에는 `0`이 올 수 없다.
- 정수는 짝수여야 한다.

요구사항을 충족하는 정수들이 저장된 배열의 요소들은 오름차순으로 정렬되어야 한다.
### 입력제한
- 3 <= digits.length <= 100
- 0 <= digits[i] <= 9
### 풀이핵심
- 주어진 정수 배열의 요소를 조합해 구할 수 있는 세 자리면서 짝수인 정수들을 구해야한다.
### 문제풀이
1. 첫 째자리 수를 정한다.
   - 첫 째자리에는 `0`이 올 수 없으므로 `0`일 경우 연산을 진행하지 않는다.
   - 첫 째자리에 올 요소의 인덱스를 `exceptIndex1`에 저장한다.
   - `요소 × 100`의 결과를 `number`에 저장한다.
2. 둘 째자리 수를 정한다.
   - `exceptIndex1`와 같지 않은 인덱스를 가진 요소들만 사용한다.
   - 둘 째자리에 올 요소의 인덱스를 `exceptIndex2`에 저장한다.
   - `요소 × 10 + number`의 결과를 `number2`에 저장한다.
3. 셋 째자리 수를 정한다.
   - `exceptIndex1`와 `exceptIndex2`, 둘 모두와 같지 않은 인덱스를 가진 요소들만 사용한다.
   - `요소 + number`의 결과가 짝수인지를 확인 한 후 맞다면 `result`에 추가한다.
4. `1 ~ 3`의 과정을 반복 후 `result`의 요소들의 중복을 제거하고 오름차순으로 정렬해 반환한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/finding-3-digit-even-numbers/)
### 태그
`반복문` `배열` `다시 풀어봐야 할 문제`