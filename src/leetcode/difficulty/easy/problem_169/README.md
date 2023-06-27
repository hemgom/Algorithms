# 169. Majority Element
크기가 `n`인 정수형 배열 `nums`가 주어질 때 `다수 요소`를 반환한다.  
- `다수 요소`란, 배열 내에서 개수가 `[n / 2]`이상인 요소를 뜻한다.  
- `다수 요소`는 배열에 반드시 존재한다고 가정한다.
### 입력제한
- n == nums.length
- 1 <= n <= 5 * 10⁴
- -10<sup>9</sup> <= nums[i] <= 10<sup>9</sup>
### 풀이핵심
- 기준 값`(nums.length/2)`을 구하고 개수가 해당 값보다 크거나 같은 요소를 반환한다.
- 하지만 문제가 허술한 점이 있다. 다수 요소가 2개 이상일 경우에 대한 이야기가 없다.
- 문제를 잘못 이해한 것일 수도 있지만 문제에 부가적 설명 또는 조건이 부족한건 확실하다.
### 문제풀이
1. 기준 값`(nums.length/2)`을 구해준다.
2. 주어진 배열 `nums`에서 중복을 제거하여 요소 종류를 구한다.
3. 특정 요소와 `nums`를 비교해 요소의 개수를 구하고 기준 값 보다 크거나 같은지 확인한다.
   - 참 이라면 `result`에 저장 후 반환한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/majority-element/)
### 태그
`HashSet` `반복문` `배열 중복요소 제거 및 카운팅`