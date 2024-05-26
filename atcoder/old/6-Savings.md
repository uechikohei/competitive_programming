# [B - Savings]()https://atcoder.jp/contests/abc206/tasks/abc206_b
2022/12/19 22:47
## Anwer
    """
    シカのAtCoDeerくんは、空の貯金箱を持っています。
    AtCoDeerくんは、その貯金箱に、1 日目の朝に 1 円、2 日目の朝に 2 円 … というように、i 日目の朝に i 円を貯金箱に入れます。
    また、AtCoDeerくんは、毎日夜に貯金箱にいくら入っているかを確認します。
    AtCoDeerくんが貯金箱に N 円以上入っていることを初めて確認するのは、何日目の夜でしょうか?
    """

    n = int(input())

    money = 0
    day = 1


    while money < n:
        money += day
        if money >= n:
            #整数として出力
            print(int(day))
        else:
            day += 1
> 