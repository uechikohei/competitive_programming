# [Biscuit Generator](https://atcoder.jp/contests/abc125/tasks/abc125_a)
2022/12/05 8:13
## Anwer
    """
    ビスケット生産装置を起動すると、起動してから A 秒後、2A 秒後、3A 秒後、... (A の倍数秒後) に B 枚ずつビスケットを生産します。

    ビスケット生産装置を起動してから T+0.5 秒後までに生産されるビスケットの合計枚数を求めてください。
    """

    a,b,t = list(map(int,input().split()))

    #0.5秒は無視、1秒を満たさないと生産されない
    #7.5秒後つまり、7秒で何枚生産される？
    #//で整数のみを取り出す
    ans = t//a*b
        
    print(ans)
> https://blog.hamayanhamayan.com/entry/2019/04/28/082958

> https://upura.hatenablog.com/entry/2019/04/27/230953