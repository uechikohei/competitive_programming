# [We Love Golf](https://atcoder.jp/contests/abc165/tasks/abc165_a)
2022/12/14 20:37
## Anwer
    """
    ジャンボ高橋君はゴルフの練習をすることにしました。

    ジャンボ高橋君の目標は飛距離を K の倍数にすることですが、ジャンボ高橋君の出せる飛距離の範囲は A 以上 B 以下です。

    目標の達成が可能であれば OK と、不可能であれば NG と出力してください。
    """

    """
    for文を用いた「探索」で表現できる

    A以上B以下の整数値の範囲に、Kの倍数が存在するか判定

    if文短縮形では、existの中身がFalseなら偽の処理
    中身がTrueなら正の処理となる
    """

    k = int(input())

    a,b = map(int,input().split())

    exist = False

    for i in range (a,b+1):
        if i%k==0:
            exist = True


    print("OK" if exist else "NG")
> 