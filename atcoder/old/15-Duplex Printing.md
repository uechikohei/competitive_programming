# [Duplex Printing](https://atcoder.jp/contests/abc157/tasks/abc157_a)
2022/12/12 21:09
## Anwer
    """
    高橋君は、全 N ページから成る書類を両面印刷します。
    両面印刷では、1 枚の紙に 2 ページ分のデータを印刷することが出来ます。
    
    最小で何枚の紙が必要か求めてください。
    """
    
    a = int(input())
    
    if a%2==0:
        print(int(a/2))
    else:
        print(int((a/2)+1))
> 切り捨ての表現方法、割り切れる値以外は＋１