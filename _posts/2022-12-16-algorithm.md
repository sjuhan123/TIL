---
layout: single
title: "프로그래머스 Lv.0 직사각형 넓이 구하기"
categories: Algorithm
tag: [Algorithm, 프로그래머스, Lv.0]
toc : true
toc_sticky: true
toc_label: " "
toc_icon: " " 
header:
  teaser: /assets/images/알고리즘.png
---

## 알고리즘 풀이 방식

 가끔 알고리즘 문제가 안 풀릴 때, 문제를 어떻게든 풀고 싶어서 풀릴 때 까지 계속 집착하다가 결국 문제도 못 풀고 시간을 너무 낭비하는 경우가 있어, 오늘부터 알고리즘 풀 때 시간을 측정하기로 했다. 문제 풀기 1시간이 경과되면, 문제 풀이를 접고 문제 풀이를 찾아본 후 1주일 뒤 같은 요일에 다시 풀어볼 예정이다.


## 알고리즘 풀이

```js
/* 19:40분 시작, 20:22분 끝
2차원 배열의 내부 배열을 reduce와 concat으로 푼다.
풀고 나서 for문을 이용해 계산.
1. 가로길이 구하는 방법: 절대값(홀수 index끼리 뺀 값)
2. 세로길이 구하는 방법: 절대값(짝수 index끼리 뺀 값)

return 가로길이 * 세로길이
*/
function solution(dots) {
    var answer = [];
    var dotsInArray = dots.reduce((ac, cv) => ac.concat(cv));

    for(let i = 0; i < dotsInArray.length; i += 2){
      if(!(dotsInArray[i] - dotsInArray[i + 2] === 0)){
        answer.push(Math.abs(dotsInArray[i] - dotsInArray[i + 2]));
        break;
      }
    }

    for(let i = 1; i < dotsInArray.length; i += 2){
      if(!(dotsInArray[i] - dotsInArray[i + 2] === 0)){
        answer.push(Math.abs(dotsInArray[i] - dotsInArray[i + 2]));
        break;
      }
    }

    return answer[0] * answer[1];
}

console.log(solution([[1, 1], [2, 1], [2, 2], [1, 2]])); // 1
console.log(solution([[-1, -1], [1, 1], [1, -1], [-1, 1]])); // 4

// 프로그래머스 채점 통과
```

