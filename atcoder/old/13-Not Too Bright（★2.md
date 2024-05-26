# [033 - Not Too Bright（★2） ](https://atcoder.jp/contests/typical90/tasks/typical90_ag)
2022/12/13 20:15
## Anwer
    """
    E869120 くんは、冬に公開するイルミネーションを作成することを計画しています。
    E869120 くんが計画しているイルミネーションは、縦 H × 横 W の HW 個のLEDで構成されます。
    イルミネーションの各 LED は、点灯・消灯の状態を任意に切り替えることができます。

    このイルミネーションは、以下の条件を満たすとき 不適切である といいます。

    イルミネーション全体に完全に含まれる 縦 2 × 横 2 の、4 つの LED を含む領域であって、点灯している LED が領域内に 2 つ以上あるものが存在する。
    適切な（不適切な状態ではない）イルミネーションの点灯パターンのうち、点灯している LED の個数としてありうる最大値を求めてください。
    """

    # コーナーケースに気をつける
    """
    https://logicalbear.net/%E3%80%90%E7%AB%B6%E3%83%97%E3%83%AD%E5%85%B8%E5%9E%8B90%E5%95%8F%E3%80%91%E3%80%8C033-not-too-bright%EF%BC%88%E2%98%852%EF%BC%89%E3%80%8D%E8%A7%A3%E6%B3%95/

    設置できるLEDの数は？

    パターンA：
        縦要素Hか横要素Wどちかが、１の場合
        １ではない要素数分設置できる

    パターンB：
        縦要素Hか横要素W両方とも、２以上の場合
        2x2=4個の範囲が領域となり、その範囲につき１箇所しか置けない
    """


    h,w = map(int,input().split())

    if h == 1:
        answer = w
    elif w == 1:
        answer = h
    else:
        answer = ((h+1)//2)*((w+1)//2)
    print(answer)
> [解説](https://find-best-practice.com/2021/09/11/%E3%80%90atcoder%E3%80%91%E7%AB%B6%E3%83%97%E3%83%AD%E5%85%B8%E5%9E%8B%E5%95%8F%E9%A1%8C90%E5%95%8F%E3%81%AB%E6%8C%91%E6%88%A6/#toc50)

> [考え方](https://logicalbear.net/%E3%80%90%E7%AB%B6%E3%83%97%E3%83%AD%E5%85%B8%E5%9E%8B90%E5%95%8F%E3%80%91%E3%80%8C033-not-too-bright%EF%BC%88%E2%98%852%EF%BC%89%E3%80%8D%E8%A7%A3%E6%B3%95/)

> [難しいけど要は、HかWのうち一方が1のときはmax(H,W)が答えとなる。](https://well-defined.hatenadiary.com/entry/2022/05/20/122828)