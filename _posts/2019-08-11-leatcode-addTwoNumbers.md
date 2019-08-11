---
published: false
title: 'Leat Code문제, Add Two Numbers'
tags:
  - leat_code
  - algorithm
  - failed
---
leetcode의 두 번째 문제이며 난이도는 중이다.
문제의 내용은 아래와 같다.
```
You are given two non-empty linked lists representing two non-negative integers. The digits are stored in reverse order and each of their nodes contain a single digit. Add the two numbers and return it as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

Example:
Input: (2 -> 4 -> 3) + (5 -> 6 -> 4)
Output: 7 -> 0 -> 8
Explanation: 342 + 465 = 807.
```

푸는 데 실패하여 solution을 확인할 수 밖에 없었다.
예상과 다르게 재귀적인 문제가 아니였다.
while을 이용해 l1과 l2가 null이 될 때까지 내부 순환을 하면서 로직을 짜고 있었다.

해당 문제를 풀지 못한 두 가지 문제가 있다.
1. 문제를 정확하게 읽지 않아 요지를 제대로 이해하지 못했다.(영어라서 슥슥 넘겼다. 앞으로 주의하자)
2. 재귀로 풀이하는 문제일 것으로 확신했다.

Java로된 해답을 C++로 코드 컨버팅하면서 어떻게 동작하는지 확인했다.
결과적으로 문제를 풀지 못했으니 더 열심히 해야겠다..