---
published: true
permalink: leetcode-two-sum.html
tags:
  - post
title: 'Leet Code문제, Two Sum'
---
회사에서 일이 루즈하다보니 요즘 감이 떨어졌다는 생각이 들었다.

친동생이 좋은 알고리즘테스트 [사이트](https://leetcode.com)를 추천해줬다.

카카오뱅크 코드테스트를 분석한 적 있는데, 현 회사에서 주력으로 하고있는 C#언어로 시험을 볼 수 없다는 것을 알게됐다.

어쩔 수 없이 다른 언어를 선택해서 공부해야 할 것 같은데..

2년도 더 지난 예전 내 주력언어 c++이 가장 시험통과율이 높다고 한다.

그동안 C++ 손은 대지 않아 두려움까지 느껴졌지만 'Two sum' 문제를 직접 푸는 것으로 현 상태를 확인해봤다.

문제는 아래와 같다.
```
Given an array of integers, return indices of the two numbers such that they add up to a specific target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

Example:

Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].
```
역시나 감은 많이 떨어져 있었는데 vector의 사이즈 가져오는 함수조차 기억나지 않아 헤멨다.

구글링을 통하여 vector 사용법에 대해 찾아봤다.

어렵지 않은 역경이었기에 성공적으로 '통과'를 할 수 있었다.

![cpp]({{site.baseurl}}/_posts/2019-08-11-algorithm_test_two_sum-cpp.png)

내가 지금 할 수 있는 언어는 C#, python, swift, javascript, go, c++, PHP 정도이다.

여기서 알고리즘 테스트에 사용하지 않을 언어는 javascript, PHP를 생각해서 제외 시켰다.

Javascript는 nodejs로 나름 즐겁게 코딩할 수 있지만, 환경에 따라 디버깅이 어려울 수 있기 때문이다.

또 PHP는 사장될 언어로 생각해서, 첫 회사에서 다룬 후에 거들떠 보지 않았기 때문이다.

python으로 똑같은 루틴을 구성했는데.. 이럴수가!

Timeout이 방생한다.

이중 for문이 문제일거라는 생각은 들었으나 다른 단서가 생각나지 않았다.

좋은 아이디어가 떠오르지 않아서 결국 다른 사람들이 어떻게 풀엇는지 참고해봤다.

몇 가지 방법이 있었지만, 그중에 마음에 드는 방법은 for문을 돌면서 target-num[i]의 캐시를 남기는 방법이었다.

캐시 키는 num[i]이며 값은 i이다.

보통은 i를 키로 하지만 검색이 쉽게하기 위해 num[i]를 사용하고 있다.

'푸는 것은 어렵지만 해결법을 보면 어렵지 않다.' 는 생각이 들었다.

알고리즘을 많이 풀어보는 것만이 현재의 상황을 타개하는 유일한 길일 것이다.

고등학교 때 선생님이 오답노트를 만들어 되새김질하면서 공부하라는 이야기가 떠올라,

블로그에 최대한 의식의 흐름에 따라 알고리즘 시험 과정을 기입하기로 결정했다.

C# 문제를 풀면서 하나 의문이 들었다.

'System.Collections.Generic' 같은 라이브러리를 사용해도 되나는 것이 의문점이다.

실무에서는 편의를 위해 무조건 사용하겠지만, 출제자의 의도에 따라 사용이 불가능할 경우가 있을 거라고 생각한다.

그렇다면 dictionary나 set 등 기본적인 자료구조를 사용할 수 있는 python이나 swift 등이 c계열보다 더 다양한 방법으로 쉽게 문제
를 풀 수 있다는 결론에 도달했다.

따라서 감을 찾기위해 C++을 기준으로 공부를 하되, 시험 상황에 따라 유리한 언어를 사용할 수 있도록 준비해야 할 것이다.

Leetcode에서는 막지 않은 것 같으므로 사용해서 풀어봤다.

python으로 풀어봤는데, for문을 돌면서 key와 value를 한꺼번에 가져오는 방법을 예전에 사용한 기억이 났다.

하지만 자세한 방법은 생각나지 않아 잠깐 구글링을 해봤다.
```python
# 인덱스 번호와 컬렉션의 원소를 tuple 형태로 반환
for idx, value in enumerate(s):
	print("idx : {}, value: {}".format(idx, value))
```

swift에서 막혔던 부분은 dictionary에 key가 존재하는지 확인하는 부분이었다.
C#처럼 ContainsKey 함수는 존재하지 않고 아래처럼 간단하게 key가 존재하는 지 체크할 수 있었다
```swift
if cache['key'] != nil {
}
```

{% include links.html %}
