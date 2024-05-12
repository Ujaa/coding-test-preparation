# Day 1 사칙연산
## 두 수의 합
```js
function solution(num1, num2) {
    return num1 + num2;
}
```

## 두 수의 차
```js
function solution(num1, num2) {
    return num1 - num2;
}
```

## 두 수의 곱
```js
function solution(num1, num2) {
    return num1 * num2;
}
```

## 몫 구하기
```js
function solution(num1, num2) {
    return Math.floor(num1 / num2);
}
```
### Floor, Ceil

# Day 2 사칙연산, 조건문, 배열
## 두 수의 나눗셈
```js
function solution(num1, num2) {
    return Math.floor(num1 / num2 * 1000);
}
```

## 숫자 비교하기
```js
function solution(num1, num2) {
    return num1 === num2 ? 1 : -1;
}
```

## 분수의 덧셈
```js
function solution(numer1, denom1, numer2, denom2) {
    const numer = numer1 * denom2 + numer2 * denom1;
    const denom = denom1 * denom2;
    
    let gcd = 1;
    
    for(let x = 2; x <= Math.min(numer, denom); x++){
        if(numer % x === 0 && denom % x === 0)
            gcd = x;
    }
    
    return [numer/gcd, denom/gcd];
}
```
### 최대공약수 구하는 법

## 배열 두 배 만들기
```js
function solution(numbers) {
    return numbers.map((x) => x * 2);
}
```
### forEach, map

# Day 1
## 
```js

```

## 
```js

```

## 
```js

```

## 
```js

```

# Day 1
## 
```js

```

## 
```js

```

## 
```js

```

## 
```js

```

# Day 1
## 
```js

```

## 
```js

```

## 
```js

```

## 
```js

```

# Day 1
## 
```js

```

## 
```js

```

## 
```js

```

## 
```js

```

# Day 1
## 
```js

```

## 
```js

```

## 
```js

```

## 
```js

```

# Day 1
## 
```js

```

## 
```js

```

## 
```js

```

## 
```js

```

# Day 1
## 
```js

```

## 
```js

```

## 
```js

```

## 
```js

```

# Day 1
## 
```js

```

## 
```js

```

## 
```js

```

## 
```js

```
