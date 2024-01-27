# 2024-algorithm-c

## chap03 검색 알고리즘

- 선형 검색
    - 맨 앞부터 인덱스를 순서대로 검색
    - 종료 조건: 인덱스가 마지막에 도달 or 원하는 값을 찾음 (`a[i] == key`)
    - 모든 인덱스에서 종료 조건 2가지에 대한 확인이 필요함
    - (개선안) 보초법: 맨 마지막에 찾는 값을 넣어서 종료 조건을 하나로 줄인다.

```c
  int search(int a[], int n, int key)
  {
      int i = 0;
      a[n] = key;         // 보초를 추가
      while (1) {
          if (a[i] == key)
              break;      // 원하는 키값을 찾은 경우
          i++;
      }
      return i == n ? -1 : i;
  }
```
