# Day 1. 출력
## 1. 문자열 출력하기
### 문제 설명
문자열 str이 주어질 때, str을 출력하는 코드를 작성해 보세요.

### 제한사항
1 ≤ str의 길이 ≤ 1,000,000
str에는 공백이 없으며, 첫째 줄에 한 줄로만 주어집니다.

### 입출력 예
#### 입력 #1
HelloWorld!
#### 출력 #1
HelloWorld!

### 작성한 코드
```js
const readline = require('readline'); //외부 모듈 가져오기
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = [line];
}).on('close',function(){
    str = input[0];
    console.log(str);
});
```
### 보완한 코드
```
```
#### 이유

## 2. a와 b 출력하기
정수 a와 b가 주어집니다. 각 수를 입력받아 입출력 예와 같은 형식으로 출력하는 코드를 작성해 보세요.

제한사항
-100,000 ≤ a, b ≤ 100,000
입출력 예
입력 #1

4 5
출력 #1

a = 4
b = 5

```js
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    console.log(`a = ${input[0]}`);
    console.log(`b = ${input[1]}`);
});
```
## 3. 문자열 반복해서 출력하기
문제 설명
문자열 str과 정수 n이 주어집니다.
str이 n번 반복된 문자열을 만들어 출력하는 코드를 작성해 보세요.

제한사항
1 ≤ str의 길이 ≤ 10
1 ≤ n ≤ 5
입출력 예
입력 #1

string 5
출력 #1

stringstringstringstringstring

```js
const readline = require('readline');
const rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout
});

let input = [];

rl.on('line', function (line) {
    input = line.split(' ');
}).on('close', function () {
    str = input[0];
    n = Number(input[1]);
    console.log(str.repeat(n));
});
```
## 4. 대소문자 바꿔서 출력하기
## 5. 특수문자 출력하기
