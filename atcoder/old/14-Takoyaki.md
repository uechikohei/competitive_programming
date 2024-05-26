# [Takoyaki](https://atcoder.jp/contests/abc176/tasks/abc176_a)
2022/12/12 22:12
## Anwer
    """
    高橋君はたこ焼きが好きです。

    たこ焼き器を使うと、1 度に最大で X 個のたこ焼きを作ることができます。
    これにかかる時間は作る個数によらず T 分です。

    N 個のたこ焼きを作るためには何分必要ですか？
    """
    n,x,t = map(int,input().split())

    if n%x ==0:
        #割り切れるとき
        nx = (int(n/x))
        print(nx*t)
    else:
    #割り切れないとき、切り捨て（＋１で表現）
        nx = (int(n/x)+1)
        print(nx*t)
> 切り捨ての表現方法、割り切れる値以外は＋１