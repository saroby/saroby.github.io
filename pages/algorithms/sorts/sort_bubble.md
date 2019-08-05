---
title: 삽입 정렬
keywords: algorithm, sort, 정렬
sidebar: algorithm_sidebar
permalink: insertion_sort.html
folder: algorithms/sorts
---

## 삽입 정렬(insertion sort)
두 번째 인덱스를 선택한다.
인덱스에 존해하는 숫자를 저장.
인덱스보다 왼쪽에 있는 숫자들 비교하되, 우측에서 좌측으로 하나씩 비교한다.
저장된 숫자보다 비교하는 숫자가 작으면 해당 위치에 해당 숫자를 저장하고, 위치+1에 비교된 값을 저장한다.
즉 한개씩 뒤로 민다.
더이상 밀 수 없고 다음 인덱스가 존재한다면, 인덱스를 증가시킨다.

void insertion_sort (int *data, int n)
{
  int i, j, remember;
  for ( i = 1; i < n; i++ ) {
    remember = data[(j=i)];
    while ( --j >= 0 && remember < data[j] ) {
        data[j+1] = data[j];
        data[j] = remember;
    }
  }
}


{% include links.html %}
