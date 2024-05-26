# [Buying Sweets](https://atcoder.jp/contests/abc087/tasks/abc087_a)
2022/12/01 21:59
## Anwer
    x,a,b = [int(input()) for i in range (3)]
    ax = x-a

    # axがbより多い、かつaxがbと等しいとき→True
    while ax >= b:
        # True条件式
        # axからbの値を引いて,axに代入（ずっとcに代入し出力してエラー詰まった）
        ax = ax - b
    # 出力もax、インデントによりwhileによる繰り返しが終わったときに処理される箇所。
    print(ax)
> 