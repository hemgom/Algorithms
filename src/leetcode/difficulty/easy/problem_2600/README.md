# 2600. K Items With the Maximum Sum
아이템 3개가 존재하고, 각 아이템은 숫자 `1`, `0`, `-1`을 가진다.  
4개의 음이 아닌 정수 `numOnes`, `numZeros`, `numNegOnes`, `k`가 주어진다.

주어진 변수는 다음을 뜻한다.  
`numOnes`는 아이템 `1`의 개수를 의미한다.  
`numZeros`는 아이템 `0`의 개수를 의미한다.  
`numNegOnes`는 아이템 `-1`의 개수를 의미한다.  
`k`는 전체 아이템의 개수 중 선택할 개수를 의미한다.

각 변수가 주어질 때 선택한 아이템의 합이 최대가 되도록 선택하고 그 `최대 합`을 반환한다.
### 입력제한
- 0 <= `numOnes`, `numZeros`, `numNegOnes` <= 50
- 0 <= `k` <= `numOnes + numZeros + numNegOnes`
### 풀이핵심
결국 `최대 합`을 구하려면 높은 숫자를 가진 아이템부터 사용하면 된다.  
`1`을 먼저 사용하고 그 다음 `0` 그리고 `-1` 순으로 사용해준다.
### 문제풀이
- 메서드는 2개를 사용했다. A-`k의 값 만큼 배열에서 값을 가져와 연산하는 메서드`, B-`배열에 아이템을 저장하는 메서드`
- `아이템 0`의 경우 정수형 배열의 초기화 값이 `0`이므로 따로 연산하지 않았다.
1. 아이템의 총 합만큼의 길이를 가진 정수형 배열을 생성한다.
2. 각 아이템(`1`, `-1`)이 저장될 시작 인덱스를 변수로 선언한다 -> `oneStart`, `negOneStart`
3. `B 메서드`를 통해 배열에 아이템을 배치 저장한다.
4. `for 문`을 사용해 필요한 개수(`k`)만큼 배열에서 값을 꺼내 `reuslt`에 더한다. 
### 문제출처
- [leetcode](https://leetcode.com/problems/k-items-with-the-maximum-sum/)
### 태그
`배열` `오버로딩`