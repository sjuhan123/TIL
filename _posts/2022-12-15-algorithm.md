---
layout: single
title: "프로그래머스 Lv.0 삼각형의 완성조건"
categories: Algorithm
tag: [Algorithm, 프로그래머스, Lv.0]
toc : true
toc_sticky: true
toc_label: " "
toc_icon: " " 
header:
  teaser: /assets/images/알고리즘.png
---

문제를 읽고 우선 return 할 변수 answer가 어떤 경우에 증가할지 경우에 따라서 나눈 후 문제를 풀었다.

```js
/*
나머지 한변이 될 수 있는 정수는 
1. 두 변 중에 한 변이 제일 길 때, 나머지 한 변은
두 변의 차이보다 크거나 제일 긴 변보다 작거나 같아야 되고,
2. 나머지 한 변이 제일 길 때는, 두 변 보다 길거나 두 변의 합보다 작아야 된다.
*/

function solution(sides){
  var answer = 0;
  var minus = Math.abs(sides[0] - sides[1]);
  
  for(let i = minus + 1; i <= Math.max(...sides); i++){
    answer += 1;
  }

  var plus = sides.reduce((accumulater, currentValue) => accumulater + currentValue, 0);

  for(let i = Math.max(...sides) + 1; i < plus; i++){
    answer += 1;
  }
  return answer;
}

console.log(solution([1,2])); // 1
console.log(solution([3,6])); // 5
console.log(solution([11,7])); // 13
```