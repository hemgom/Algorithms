# 283. Move Zeroes
정부 배열의 숫자가 주어질 때, `0`이 아닌 요소의 숫자의 경우 기존 순서를 유지하고  
모든 `0`의 경우에는 배열의 끝으로 이동한다.

배열의 복사본을 반들지 않고 작업을 수행해야한다.
### 입력제한
- 1 <= nums.length <= 10⁴
- -2ⁿ <= nums[i] <= 2ⁿ - 1 (n = 31)
### 풀이핵심
복사본을 만들지 말고 입력 받은 배열의 요소를 수정해야한다.
### 문제풀이
- `0`이 아닌 요소의 개수를 반환하는 `notZeroCount()` 메서드를 구현하고 사용한다.
- `0`이 아닌 요소를 저장한 배열을 반환한는 `notZero()` 메서드를 구현하고 사용한다.
1. `0`이 아닌 요소의 갯수와 배열을 구한다.
2. (1)에서 반환받은 `notZeroNums`의 길이 만큼 `nums`에 `0`이 아닌 요소를 저장한다.
3. (2)과정 이후 `nums`의 수정되지 않은 저장 공간에 모두 `0`을 저장한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/move-zeroes/)
### 태그
`배열`