# 2129. Capitalize the Title
공백으로 구분되는 하나 이상의 단어로 구성되는 문자열 `title`이 주어진다.  
문자열의 단어는 `영문자(소문자 or 대문자)`로 구성될 때  
단어의 길이에 따라 `단어`가 가진 대소문자를 변경한다.  

단어의 길이가 `1` or `2`인 경우 모든 글자를 소문자로 변경  
단어의 길이가 `3`이상이면 첫 글자를 대문자 나머지는 소문자로 변경  

변경된 제목을 반환한다.
### 입력제한
- 1 <= title.length <= 100
- `title`은 선행 또는 후행에 공백이 올 수 없으며, 공백을 구분자로 한다.
- 각 단어는 영어 대문자와 소문자로 구성된다.
### 풀이핵심
문자열을 단어 단위로 구분지어 순차적으로 요구사항에 맞게 변환한다.
### 문제풀이
- `capitalizeTitle`메서드를 `오버로딩`하여 활용한다.
- `String.toUpperCase()` : 문자열의 영소문자를 모두 영대문자로 바꾼다.
- `String.toLowerCase()` : 문자열의 영대문자를 모두 영소문자로 바꾼다.
1. `title`을 순차적으로 `char` 단위로 읽는다.
2. `' '(공백)` 문자일 경우 `imptyIndex`에 해당 공백문자의 인덱스를 저장한다.
3. 오버로딩한 `capitalizeTitle`메서드를 호출해 문자열을 반환 받아 `result`에 저장한다.
   - 문자열 저장 시 뒤에 `" "(공백 문자열)`을 붙여 저장한다.
4. `wordStartIndex`에 다음 단어 첫 글자의 인덱스를 저장한다.
   - 다음 단어 첫 글자 인덱스 = 공백 문자의 인덱스 +1
5. 마지막 공백 이후의 마지막 단어를 연산해 `result`에 저장한다.
### 문제출처
- [leetcode](https://leetcode.com/problems/capitalize-the-title/)
### 태그
`오버로딩(overloading)` `문자열` `toUpperCase(), toLowerCase()`