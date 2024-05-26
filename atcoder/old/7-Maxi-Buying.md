# [Maxi-Buying](https://atcoder.jp/contests/abc206/tasks/abc206_a)
2022/12/17 15:45
## Anwer
    """
    ABC 国の消費税率は 8 パーセントです。
    ABC 国にはエナジードリンク屋さんがあります。ここでは、エナジードリンク 1 本を、税抜き N 円で販売しています。
    ここに消費税を加算した後の金額は ⌊1.08×N⌋ 円となります。ただし、実数 x に対し、⌊x⌋ は x 以下の最大の整数を表します。
    この金額が定価の 206 円より安いなら Yay! 、定価と等しいなら so-so 、定価より高いなら :( と出力して下さい。
    """

    n = int(input())

    an = int(1.08*n)

    if an < 206:
        print("Yay!")
    elif an == 206:
        print("so-so")
    else:
        print(":(")
> 