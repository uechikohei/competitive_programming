# [Some Sums](https://atcoder.jp/contests/abc083/tasks/abc083_b)
2022/12/16 0:03
## Anwer
    """
    1 以上 N 以下の整数のうち、10 進法での各桁の和が A 以上 B 以下であるものの総和を求めてください。
    """
    n,a,b = map(int,input().split())

    # 整数nの各桁の和を求める関数を作成する
    # 関数はcalc_sum_digits
    # 引数はn
    # 返り値はsum_digit
    def calc_sum_digits(n):
        # 返り値の初期化
        sum_digit = 0
        # 引数nが0より大きい場合は処理を継続
        while n > 0:
            # 10で割った余り値（１桁目を抽出している）を足している
            sum_digit += n % 10
            # 10で割った値（１桁目を排除）
            n//= 10
        # 返り値に引数nの各桁の和が代入される
        return sum_digit

    # 答えを格納する変数（総和）
    result = 0

    # 1以上n以下の整数iを調べていく
    for i in range(1,n+1):
        # 各桁の和がA以上、B以下である場合は加算
        if a <= calc_sum_digits(i) <= b:
            result += i
    # 出力となる
    print(result)
> 