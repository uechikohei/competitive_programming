# [Serval vs Monster](https://atcoder.jp/contests/abc153/tasks/abc153_a)
2022/11/26 23:39
## Anwer
    a,b = map(int, input().split())

    if a % b ==0:
        print(a//b)
    else:
        print(a/b+1)
> 