# [Apple Pie](https://atcoder.jp/contests/abc128/tasks/abc128_a)
2022/12/04 22:44
## Anwer
    a,p = map(int,input().split())

    q = (p+(a*3))

    counter = 0

    while q > 1:
        q -= 2
        
        counter += 1

    print(counter)
> 