
# [D087:文字をくっつける](https://paiza.jp/challenges/224/show)
2022/12/08 8:18
## Anwer
    """
    高橋君は、全 N ページから成る書類を両面印刷します。
    両面印刷では、1 枚の紙に 2 ページ分のデータを印刷することが出来ます。

    最小で何枚の紙が必要か求めてください。
    """

    a = int(input())

    #roundによる四捨五入ではなく、intで切り捨て値を1増やして表現
    if a%2==0:
        print(int(a/2))
    else:
        print(int((a/2)+1))
> 
# [D197:買い物のポイント](https://paiza.jp/career/challenges/501/retry)
2022/12/07 8:34
## Anwer
    a = int(input())

    if a >= 1000:
        print(int(a*0.1))
    else:
        print(0)
> 


# [D219:犬猿の仲](https://paiza.jp/career/challenges/565/retry)
2022/12/07 8:25
## Anwer
    a = input()
    b = ("saru")
    #文字列をあらかじめ大文字、または小文字に変換することで大文字小文字を区別することなく比較する

    if a.lower() != b.lower():
        print("Yes")
    else:
        print("No")
> 


# [D133:株の利益](https://paiza.jp/career/challenges/331/retry)
2022/12/06 22:38
## Anwer
    x,a,b = [int(input()) for i in range (3)]

    counter = 0

    while x >= a:
        
        x = x-a
        
        counter+=1
> 

    
print((counter*b)-(counter*a))
# [D143:制動距離の計算](https://paiza.jp/challenges/352/ready)
2022/12/05 22:15
## Anwer
    m,v,f = map(int,input().split())

    a = m*(v*v)/(2*f)

    print(int(a))
> 
# [D134:タイトルの長さ](https://paiza.jp/challenges/332/show)
2022/12/05 0:08
## Anwer
    """
    表紙に印刷する文字列 S が与えられるので 10 文字ごとに改行して出力するプログラムを作成してください。
    """

    a = str(input())

    #ステップ値を10を指定。10文字列ごとに1度の処理
    for i in range(0,len(a),10):
        #n回目→開始値がn番目〜終了値がn+10番目(ステップ10指定のため)
        print(a[i : i + 10])
> sliceの使い方を覚える

> lenで要素数をカウントする

> for文での繰り返し変数iをうまく使う

> rangeやsliceでの、ステップ値の概念を抑える



# [D086:門松の作成](https://paiza.jp/challenges/222/ready)
2022/12/03 21:39
## Anwer
    a = int(input())
    #比率を入力
    b,c,d = (3,5,7)
    #1割の長さを算出。※ここでintで括ったりroundで四捨五入すると出力で誤差出現する
    e = (a/3)
    #1割の長さfloat型で計算後、roundで四捨五入することで誤差がなくなる
    print(round(e*15))
> 
# [D004:文字列の結合](https://paiza.jp/career/challenges/36/retry)
2022/12/02 23:24
## Anwer
    #後述for文で繰り返す数
    a = int(input())

    #for文でbに文字列をリストで格納
    b = [input() for i in range(a)]

    #for文、bにインデックス付与
    for i, e in enumerate(b):
        #インデックスの値が0のとき（1文字目の処理）
        if i == 0:
            #以下内容を出力
            print("Hello", end=" ")
        #eに代入した要素をすべて出力
        print(e, end="")
        #i番目が、[b要素の数-1]番目(5要素であれば、-1で4番目を表現)
        #つまり、最終文字の処理は"."それ以外は","を付与
        if i == len(b) -1:
            print(".")
        else:
            print(",",end="")
> enumerateによるインデックス付与

> lenによる要素数のカウント

> -1付与し、最終処理を分岐する

> [神記事](http://taustation.com/python3-for-loop-first-and-last-execution/)

# [D003:掛け算のリスト](https://paiza.jp/career/challenges/34/retry)
2022/12/01 21:55
## Anwer
    a = int(input())

    for i in range(1,10):
        if i == 9:
            print(a*i, end="")
        else:
            print(a*i, end=" ")
> for文では、range(1,10)で1~9の数値に対して処理をすることが可能

> if i == 9:で9の値で分岐し処理する（つまり、最後だけ処理する）

> end=" "で終端に修飾できる

# [D228:【2022年Xmas問題】クリスマスの時間](https://paiza.jp/career/challenges/593/retry)
2022/11/30 20:55
## Anwer
    import datetime
    a,b = map(int,input().split())
    c,d = map(int,input().split())

    sunset = datetime.datetime(2022,12,25,a,b)
    now = datetime.datetime(2022,12,25,c,d)

    if now >= sunset:
        print("No")
    else:
        print("Yes")
> import文

> datetimeメソッドの使用

> 時系列によるif文の分岐

# [D084:英語で何月？](https://paiza.jp/career/challenges/216/retry)
2022/11/29 21:38
## Anwer
    a = input()

    d = {1:'January',2:'February',3:'March',4:'April',
    5:'May',6:'June',7:'July',8:'August',9:'September',
    10:'October',11:'November',12:'December'}

    value = d[int(a)]

    print(value)
> 

# [D002:数の比較](https://paiza.jp/career/challenges/31/retry)
2022/11/28 23:19
## Anwer
    a,b = map(int, input().split())

    if a == b:
        print("eq")
    elif a > b:
        print(a)
    else:
        print(b)
> 

# [D101:偶数派と奇数派](https://paiza.jp/career/challenges/258/retry)
2022/11/27 20:55
## Anwer
    a,b = map(int, input().split())

    if a%2==0 and b%2==0:
        print("NO")
    elif a%2==1 and b%2==1:
        print("NO")
    else:
        print("YES")
> 

# [D213:タイプ数の予想](https://paiza.jp/career/challenges/552/retry)
2022/11/26 23:39
## Anwer
    a = int(input())
    print(a*365)
> 

# [D194:カロリーの計算](https://paiza.jp/challenges/487/ready)
2022/11/25 22:42
## Anwer
    a = int(input())
    print(a*540)
> 

# [D227:引き落としの手数料](https://paiza.jp/challenges/592/ready)
2022/11/24 23:30
## Anwer
    a = int(input())
    print(a-120)
> 1行かつ1つの値を入力する