# [Infinite Coins](https://atcoder.jp/contests/abc088/tasks/abc088_a)
2022/11/30 20:55
## Anwer
    a = [int(input()) for i in range(2)]
    b = (int(a[0]/500))

    if (a[0]-(b*500)) <= a[1]:
        print("Yes")
    else:
        print("No")
> 