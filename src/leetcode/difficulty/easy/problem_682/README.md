# 682. Baseball Game
특이한 규칙이 있는 야구 경기의 점수를 기록 중이다. 처음에는 `빈 기록`으로 시작한다.  
문자열 배열 `operations`가 주어지며, `operations[i]`는 레코드에 적용해야하는 `i`번째 연산이다.  
연산의 종류는 아래와 같다.
- 정수 `x` : 새로운 점수 `x`를 기록한다.
- `"+"` : 최근 점수 2개를 더해 기록한다.
- `"D"` : 가장 최근 점수의 2배를 기록한다.
- `"C"` : 가장 최근 점수를 제거한다.

최종 기록된 모든 점수를 더해 반환한다.  
(테스트 케이스는 답과 모든 중간 계산이 32비트 정수에 해당하며, 모든 연산이 유효하도록 생성된다.)
### 입력제한
- 1 <= `operations.length` <= 1000
- `operations[i]`는 `"C"` `"D"` `"+"` 또는 `[-3 * 10⁴, 3 * 10⁴]`범위의 정수를 나타내는 문자열이다.
- `"+"`가 있는 경우, 항상 2개 이상의 점수가 기록되어 있다.
- `"C"` `"D"`가 있는 경우, 항상 1개 이상의 점수가 기록되어 있다.
### 풀이핵심
- `operations`의 요소에 따라 순차적으로 연산을 진행하고 기록된 모든 점수를 더해 반환한다.
### 문제풀이
1. `List<Integer> record`를 생성해 점수를 기록한다.
2. `operations`의 모든 요소(operation)에 대해 아래의 연산을 수행한다.
   - `record`의 마지막 인덱스를 `lastIndex`에 저장한다.
   - `"+"`인 경우 : `record.get(lastIndex)`와 `record.get(lastIndex-1)`을 더해 `record`에 추가한다.
     - 이후 다음 반복으로 넘어간다.
   - `"D"`인 경우 : `record.get(lastIndex)`의 2배를 `record`에 추가한다.
     - 이후 다음 반복으로 넘어간다.
   - `"C"`인 경우 : `record`의 마지막 요소를 삭제한다.
     - 이후 다음 반복으로 넘어간다.
   - 그 외(정수)인 경우 : `recored`에 정수 `x`를 추가한다.
3. `totalScore`를 생성해 모든 `record`의 요소를 더해 저장하고 해당 변수를 반환한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/baseball-game/)
### 태그
`배열 요소 비교` `ArrayList`