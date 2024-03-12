# Day 3. 연산, 조건문
## 16. n의 배수
### 문제 설명
정수 num과 n이 매개 변수로 주어질 때, num이 n의 배수이면 1을 return n의 배수가 아니라면 0을 return하도록 solution 함수를 완성해주세요.

### 제한사항
2 ≤ num ≤ 100
2 ≤ n ≤ 9

### 입출력 예

|num|n|result|
|---|---|---|
|98|2|1|
|34|3|0|

### 입출력 예 설명
#### 입출력 예 #1
98은 2의 배수이므로 1을 return합니다.

#### 입출력 예 #2
32는 3의 배수가 아니므로 0을 return합니다.

### 작성한 코드
```js
function solution(num, n) {
    return num % n == 0 ? 1 : 0;
}
```

### 참고할 코드
```js
function solution(num, n) {
    return num%n===0?1:0;
}
```

## 12. 문자 리스트를 문자열로 변환하기
### 문제 설명
문자들이 담겨있는 배열 arr가 주어집니다. arr의 원소들을 순서대로 이어 붙인 문자열을 return 하는 solution함수를 작성해 주세요.

### 제한사항
1 ≤ arr의 길이 ≤ 200
arr의 원소는 전부 알파벳 소문자로 이루어진 길이가 1인 문자열입니다.

### 입출력 예
|arr|result|
|---|---|
|["a","b","c"]|"abc"|

```js
function solution(arr) {
    var answer = '';
    arr.forEach((element) => answer += element);
    return answer;
}
```

### 참고할 코드
```js
function solution(arr) {
    return arr.join("")
}
```

## 13. 문자열 곱하기
### 문제 설명
문자열 my_string과 정수 k가 주어질 때, my_string을 k번 반복한 문자열을 return 하는 solution 함수를 작성해 주세요.

### 제한사항
1 ≤ my_string의 길이 ≤ 100
my_string은 영소문자로만 이루어져 있습니다.
1 ≤ k ≤ 100

### 입출력 예
|my_string|k|result|
|---|---|---|
|"string"|3|"stringstringstring"|
|"love"|10|"lovelovelovelovelovelovelovelovelovelove"|
#### 입력 #1
예제 1번의 my_string은 "string"이고 이를 3번 반복한 문자열은 "stringstringstring"이므로 이를 return 합니다.

#### 출력 #1
예제 2번의 my_string은 "love"이고 이를 10번 반복한 문자열은 "lovelovelovelovelovelovelovelovelovelove"이므로 이를 return 합니다.

```js
function solution(my_string, k) {
    return my_string.repeat(k);
}
```

## 14. 더 크게 합치기
### 문제 설명
연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.

12 ⊕ 3 = 123
3 ⊕ 12 = 312
양의 정수 a와 b가 주어졌을 때, a ⊕ b와 b ⊕ a 중 더 큰 값을 return 하는 solution 함수를 완성해 주세요.

단, a ⊕ b와 b ⊕ a가 같다면 a ⊕ b를 return 합니다.

### 제한사항
1 ≤ a, b < 10,000

### 입출력 예
|a|b|result|
|---|---|---|
|9|91|991|
|89|8|898|
#### 입력 #1
a ⊕ b = 991 이고, b ⊕ a = 919 입니다. 둘 중 더 큰 값은 991 이므로 991을 return 합니다.

#### 출력 #1
a ⊕ b = 898 이고, b ⊕ a = 889 입니다. 둘 중 더 큰 값은 898 이므로 898을 return 합니다.

```js
function solution(a, b) {
    var num1 = Number(a.toString() + b.toString());
    var num2 = Number(b.toString() + a.toString());
    return num1 >= num2 ? num1 : num2;
}
```

### 참고할 코드
```js
function solution(a, b) {
    return Math.max(Number(`${a}${b}`), Number(`${b}${a}`))
}
```

## 15. 두 수의 연산값 비교하기
### 문제 설명
연산 ⊕는 두 정수에 대한 연산으로 두 정수를 붙여서 쓴 값을 반환합니다. 예를 들면 다음과 같습니다.

12 ⊕ 3 = 123
3 ⊕ 12 = 312
양의 정수 a와 b가 주어졌을 때, a ⊕ b와 2 * a * b 중 더 큰 값을 return하는 solution 함수를 완성해 주세요.

단, a ⊕ b와 2 * a * b가 같으면 a ⊕ b를 return 합니다.

### 제한사항
1 ≤ a, b < 10,000

### 출력 예시
|a|b|result|
|---|---|---|
|2|91|364|
|91|2|912|
#### 입출력 예 #1
a ⊕ b = 291 이고, 2 * a * b = 364 입니다. 둘 중 더 큰 값은 364 이므로 364를 return 합니다.
#### 입출력 예 #2
a ⊕ b = 912 이고, 2 * a * b = 364 입니다. 둘 중 더 큰 값은 912 이므로 912를 return 합니다.

```js
function solution(a, b) {
    return Math.max(Number(`${a}${b}`), 2*a*b);
}
```
