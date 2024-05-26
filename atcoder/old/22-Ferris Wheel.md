# [Ferris Wheel](https://atcoder.jp/contests/abc127/tasks/abc127_a)
2022/11/28 23:19
## Anwer
    a,b = map(int, input().split())

    if a >= 13:
        print(b)
    elif a <= 12 and a > 5:
        print(b//2)
    elif a <= 5:
        print(0)
    else:
        print("error")
> ifによる複数分岐