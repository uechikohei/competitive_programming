# [A - Sheep and Wolves ](https://atcoder.jp/contests/abc164/tasks/abc164_a)
2023/01/05 6:45
## Anwer
    """
    羊が S 匹、狼が W 匹います。

    狼の数が羊の数以上のとき、羊は狼に襲われてしまいます。

    羊が狼に襲われるなら unsafe、襲われないなら safe を出力してください。
    """

    s, w = map(int, input().split())

    if s <= w: #数字sが数字wと同等or小さい場合
        print("unsafe")
    else:
        print("safe")
