# 496. Next Greater Element I
배열에서 `다음으로 큰 요소`는 `x`라는 요소가 있을 때  
`x`의 오른쪽에 있는 요소들 중 `x`보다 큰, 첫 번째 요소를 말한다.  

정수형 배열 `nums1`과 `nums2`가 주어지며, `nums1`은 `nums2`의 부분집합이다.

각각 `0 <= i < nums1.length`에 대해서 `nums1[i] == nums2[j]`가 되도록  
인덱스 `j`를 구하고 `nums2`에서 `nums2[j]`보다 큰 요소를 구한다.  
만약 큰 요소가 없다면 해당 경우의 답은 `-1`이다.  

`ans[i]`에 각각의 답을 저장하여 길이 `nums1.length`의 배열 `ans`를 반환한다.
### 입력제한
- 1 <= `nums1.length` <= `nums2.length` <= 1000
- 0 <= `nums1[i], nums2[i]` <= 10⁴
- `nums1`과 `nums2`의 모든 정수는 중복된 값을 갖지 않습니다.
- `nums1`은 `nums2`의 부분집합입니다.
### 풀이핵심
- 문제가 장황하지만 요약하자면
  1. `nums1`의 각 요소와 같은 요소를 `nums2`에서 찾는다.
  2. `nums2`에서 찾은 같은 요소를 기준으로 오른쪽에 있는 요소들 중 큰, 첫 번째 요소를 찾는다.
  3. 큰 요소가 있다면 그 요소를 없다면 `-1`을 `ans[i]`에 저장한다.
### 문제풀이
1. `nums1`의 각 요소들이 `nums2`에서 어떤 인덱스를 가지는지 확인한다.
2. `다음으로 큰 요소`에 해당하는 연산을 `nums2`에서 수행
3. 요소가 있다면 해당 요소를 없다면 `-1`을 `ans`에 저장한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/next-greater-element-i/)
### 태그
`반복문`