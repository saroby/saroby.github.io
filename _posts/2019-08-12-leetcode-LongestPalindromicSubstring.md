---
published: false
tags:
  - algorithm
  - leetcode
title: 'LeetCode 문제, Longest Palindromic Substring'
---
오늘은 leet code의 3~5번까지 풀어봤다.

3,4번은 회사의 짬시간에 눈으로 풀었으니 그런다고 치고라도 5번 문제는 오랜시간 풀었는데 오답이라고 계속 나왔다.

c++ 문법이 익숙하지 못한다는 핑계를 대지 못하는건, 충분한 시간을 썼다고 생각하기 때문이다.



코드를 세이브하고 내일 다시 풀어봐야겠다.


> Given a string s, find the longest palindromic substring in s. You may assume that the maximum length of s is 1000.
> Example 1:
>
> Input: "babad"
> Output: "bab"
> Note: "aba" is also a valid answer.
> Example 2:
>
> Input: "cbbd"
> Output: "bb"


```c++
#include <stdio.h>

class Solution {
public:
    string longestPalindrome(string s) {
        for (char c : s) {
            printf("%c", c);
        }
        printf("\n\n");
        
        int posI = 0;
        int posJ = 0;
        for (int i=0; i<s.size(); i++) {
            int j = getPalindromicSubString(s, i);
            if ((j-i) > (posJ - posI)) {
                posJ = j;
                posI = i;
                printf("in %d\n", (j-i));
            }
            printf("\n");
        }
/*        
        printf("\n%d %d\n\n", posI, posJ);
        for (char c : s.substr(posI, posJ - posI)) {
            printf("%c", c);
        }
*/       
        return s.substr(posI, posJ-posI);
    }
    
    int getPalindromicSubString(string s, int i) {
        if (s.size() < 1)
            return i;
        char stopChar = '\0';
        int output;
        bool hit
        for (int a=i; a<s.size(); a++) {
            printf("%c", s[a]);
            if (stopChar == '\0') {
                stopChar = s[a];
                output = a+1;
                continue;
            }
            if (s[a] == stopChar) {
                printf("\nstop\n");
                output = a+1;
                break;
            }
            if (a == s.size()-1) {
                printf(" err\n");
                return i+1;                
            }
        }        
        return output;
    }
};
```

화장실에서 Palindromic라는 단어를 찾아보았다.
'앞으로 뒤로 읽어도 똑같은 단어'라는 뜻이었다.. 문제를 잘못이해하고 있으니 오답이 나오지!
앞으로는 건성으로 문제를 파악하지 말자 제발.
