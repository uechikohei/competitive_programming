# [Lucky 7](https://atcoder.jp/contests/abc162/tasks/abc162_a)
2022/12/17 15:44
## Anwer
    """
    3 桁の整数 N が与えられます。N のいずれかの桁に数字の 7 は含まれますか？

    含まれるなら Yes を、含まれないなら No を出力してください。
    """
    n = input()

    nn = [int(i) for i in list(n)]

    if 7 in nn:
        print("true")
    else:
        print("false")
> 