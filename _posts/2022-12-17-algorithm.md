---
layout: single
title: "프로그래머스 Lv.0 등수 매기기"
categories: Algorithm
tag: [Algorithm, 프로그래머스, Lv.0]
toc : true
toc_sticky: true
toc_label: " "
toc_icon: " " 
header:
  teaser: /assets/images/알고리즘.png
---

## 알고리즘 구현 과정

이번 문제의 경우 카페에서 풀었는데, 1시간 제한 시간 내에 풀지 못했다.  
프리코스 때 배웠던 정렬 관련 문제로 추정되지만, 정확히 어떤 방식으로 풀어나가야 될지 감이 잡히지 않았다.  
이렇게 제한 시간 내에 풀지 못하면 시간이 더 있어도 문제를 제대로 풀 확률이 매우 적기 때문에, 앞으로도 이럴 경우 다른 풀이를 보지 않고 동일 문제를 1주일 내에 다시 풀어볼 예정이다.  
그리고 주어진 1주일이라는 기간 동안 정렬 공부도 하고 다른 알고리즘도 풀어보면서 이 문제의 접근 방식에 대해 고민할 생각이다.

## 알고리즘 

```js
/* 15:10 시작, 16:10 1시간 경과했지만 구현 실패.
1. map을 이용해 score 2차원 배열의 요소에 각각 접근해서, 점수의 평균을 구해 배열 반환
2. Math.max(...studentsAverage)를 이용해 max값 찾기. 해당 index 찾기
3. max 값 찾고 slice? splice?
*/

function solution(score) {
  const array = [];
  for(let i = 0; i < score.length; i++){
    array.push(" ");
  }

  var averageScoresInArray = score.map(element => (element[0] + element[1]) / 2);
  const maxScoresInArray = [];

  for(let i = 1; i <= score.length; i++){
    var maxScore = Math.max(...averageScoresInArray);
    maxScoresInArray.push(maxScore);
    var indexOfMaxScore = averageScoresInArray.indexOf(maxScore);
    
    averageScoresInArray.splice(indexOfMaxScore, 1);
    if(maxScoresInArray.includes(maxScore)){
      array.splice(indexOfMaxScore, 1, array[array.indexOf(maxScore)]);
    }
    array.splice(indexOfMaxScore, 1, i);
  }
  return array;

}
console.log(solution([[80, 70], [70, 80], [30, 50], [90, 100], [100, 90], [100, 100], [10, 30]]));
```