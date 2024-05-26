# [FizzBuzz Sum](https://atcoder.jp/contests/abc162/tasks/abc162_b)
2022/12/16 21:59
## Anwer
    """
    FizzBuzz列
    i が 3 でも 5 でも割り切れるなら
    =FizzBuzz
    そうではなく i が 3 で割り切れるなら
    =Fizz
    そうではなく i が 5 で割り切れるなら
    =Buzz
    そうではないなら、
    =i
    FizzBuzz列の N 項目までに含まれる数の和を求めてください。
    """

    n = int(input())
    # 和を求めるため変数初期化
    counter = 0
    # 1~n数までを繰り返して処理
    for i in range(1,n+1):
        # 3で割り切れる&5で割り切れる
        if i%3==0 and i%5==0:
            # 何もしない、空欄だとNG
            pass
        # 3で割り切れる
        elif i%3==0:
            # 何もしない、空欄だとNG
            pass
        # 5で割り切れる
        elif i%5==0:
            # 何もしない、空欄だとNG
            pass
        # それ以外
        else:
            # それ以外の値の和を表現
            counter += i
    # 繰り返し処理が終わったときの和を出力
    print(counter)