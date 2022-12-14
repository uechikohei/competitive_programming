# [B - Battle](https://atcoder.jp/contests/abc164/tasks/abc164_b)
2023/01/05 22:22
## Anwer
    """
    高橋君と青木君がモンスターを闘わせます。

    高橋君のモンスターは体力が A で攻撃力が B です。 青木君のモンスターは体力が C で攻撃力が D です。

    高橋君→青木君→高橋君→青木君→... の順に攻撃を行います。
    攻撃とは、相手のモンスターの体力の値を自分のモンスターの攻撃力のぶんだけ減らすことをいいます。
    このことをどちらかのモンスターの体力が 0 以下になるまで続けたとき
    先に自分のモンスターの体力が 0 以下になった方の負け、そうでない方の勝ちです。

    高橋君が勝つなら Yes、負けるなら No を出力してください。

    解説：https://qiita.com/u2dayo/items/ed686afffea40c9253ba#b%E5%95%8F%E9%A1%8Cbattle
    """

    a, b, c, d = map(int, input().split())

    # 先行が生き残るターン数
    # 体力÷攻撃力の切り上げを求める
    senkou = (a + d - 1) // d

    # 後攻が生き残るターン数
    # 体力÷攻撃力の切り上げを求める
    koukou = (c + b - 1) // b
    if senkou >= koukou:
        print("Yes")
    else:
        print("No")


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
> 
# [B - 200th ABC-200](https://atcoder.jp/contests/abc200/tasks/abc200_b)
2023/01/05 6:17
## Anwer
> 
    """
    整数 N が与えられます。
    以下の操作を K 回行った後の整数 N を出力してください。

    整数 N が 200 の倍数であれば、N を 200 で割る。
    そうでなければ、整数 N を、N の後ろに文字列として 200 を付け加えた整数に置き換える。
    例えば、7 を置き換えると 7200 に、1234 を置き換えると 1234200 になります。
    """

    n, k = map(int, input().split())

    for i in range(k):
        # 数字nを200で割って「0」だった場合、TRUE
        if n % 200 == 0:
            # 数字nを200で割った値をnに代入
            n //= 200
        # 数字nを200で割って「0」ではない場合、FALSE
        else:
            # 整数nを文字列変換して末尾に200という文字列追加
            s = str(n) + "200"
            # 文字列sを整数型に変換
            n = int(s)
            # 整数型の変数mを出力
    print(n)

# [A - Century](https://atcoder.jp/contests/abc200/tasks/abc200_a)
2023/01/04 6:54
## Anwer
    """
    西暦 N 年は何世紀ですか？

    世紀とは？
    西暦 1 年から 100 年までを 1 世紀、 101 年から 200 年までを 2 世紀と、
    以降も同様に西暦を 100 年単位で区切って呼称したものです。
    制約
    1≤N≤3000
    """


    n = int(input())

    print((n + 99) // 100)

> 与えられた年に+99。100で割った値（少数不使用）が世紀となる。

# [B - 1%](https://atcoder.jp/contests/abc165/tasks/abc165_b)
2022/12/20 22:42
## Anwer
    """
    高橋くんはAtCoder銀行に 100 円を預けています。

    AtCoder銀行では、毎年預金額の 1 % の利子がつきます(複利、小数点以下切り捨て)。

    利子以外の要因で預金額が変化することはないと仮定したとき、高橋くんの預金額が初めて X 円以上になるのは何年後でしょうか。
    """

    x = int(input())

    year = 0
    money = 100


    while money < x:
        money *= 1.01
        money = int(money)
        year += 1
    print(year)
> 

# [B - Savings]()https://atcoder.jp/contests/abc206/tasks/abc206_b
2022/12/19 22:47
## Anwer
    """
    シカのAtCoDeerくんは、空の貯金箱を持っています。
    AtCoDeerくんは、その貯金箱に、1 日目の朝に 1 円、2 日目の朝に 2 円 … というように、i 日目の朝に i 円を貯金箱に入れます。
    また、AtCoDeerくんは、毎日夜に貯金箱にいくら入っているかを確認します。
    AtCoDeerくんが貯金箱に N 円以上入っていることを初めて確認するのは、何日目の夜でしょうか?
    """

    n = int(input())

    money = 0
    day = 1


    while money < n:
        money += day
        if money >= n:
            #整数として出力
            print(int(day))
        else:
            day += 1
> 


# [Maxi-Buying](https://atcoder.jp/contests/abc206/tasks/abc206_a)
2022/12/17 15:45
## Anwer
    """
    ABC 国の消費税率は 8 パーセントです。
    ABC 国にはエナジードリンク屋さんがあります。ここでは、エナジードリンク 1 本を、税抜き N 円で販売しています。
    ここに消費税を加算した後の金額は ⌊1.08×N⌋ 円となります。ただし、実数 x に対し、⌊x⌋ は x 以下の最大の整数を表します。
    この金額が定価の 206 円より安いなら Yay! 、定価と等しいなら so-so 、定価より高いなら :( と出力して下さい。
    """

    n = int(input())

    an = int(1.08*n)

    if an < 206:
        print("Yay!")
    elif an == 206:
        print("so-so")
    else:
        print(":(")
> 

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
> 

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
# [今更基本的なFizzBuzz]()
2022/12/14 20:37
## Anwer
    """
    FizzBuzz

    3でも5でも割り切れる整数：FizzBuzz
    それ以外の整数の内、3で割り切れる整数：Fizz
    それ以外の整数の内、5で割り切れる整数：Buzz
    それ以外の整数：その値を出力
    """

    a = int(input())

    if a%3==0 and a%5==0:
        print("FizzBuzz")
    elif a%3==0:
        print("Fizz")
    elif a%5==0:
        print("Buzz")
    else:
        print(a)
> 

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

# [Payment](https://atcoder.jp/contests/abc173/tasks/abc173_a)
2022/12/06 8:20
## Anwer
> 
    """
    お店で N 円の商品を買います。

    1000 円札のみを使って支払いを行う時、お釣りはいくらになりますか？

    ただし、必要最小限の枚数の 1000 円札で支払いを行うものとします。
    """

    a = int(input())

    #余りが0のとき、0出力
    if (a%1000) == 0:
        print(0)
    #0以外の場合、1000円から余りを引いて出力
    else:
        print(1000-(a%1000))
# [Biscuit Generator](https://atcoder.jp/contests/abc125/tasks/abc125_a)
2022/12/05 8:13
## Anwer
    """
    ビスケット生産装置を起動すると、起動してから A 秒後、2A 秒後、3A 秒後、... (A の倍数秒後) に B 枚ずつビスケットを生産します。

    ビスケット生産装置を起動してから T+0.5 秒後までに生産されるビスケットの合計枚数を求めてください。
    """

    a,b,t = list(map(int,input().split()))

    #0.5秒は無視、1秒を満たさないと生産されない
    #7.5秒後つまり、7秒で何枚生産される？
    #//で整数のみを取り出す
    ans = t//a*b
        
    print(ans)
> https://blog.hamayanhamayan.com/entry/2019/04/28/082958

> https://upura.hatenablog.com/entry/2019/04/27/230953

# [Apple Pie](https://atcoder.jp/contests/abc128/tasks/abc128_a)
2022/12/04 22:44
## Anwer
    a,p = map(int,input().split())

    q = (p+(a*3))

    counter = 0

    while q > 1:
        q -= 2
        
        counter += 1

    print(counter)
> 


# [RGB Cards](https://atcoder.jp/contests/abc064/tasks/abc064_a)
2022/12/03 21:26
## Anwer
    #int型では結合できないので、str型で入力
    r,g,b = map(str,input().split())
    #結合したので、int型へ変換
    a = int(r+g+b)

    #4の倍数で分岐
    if a % 4 == 0:
        #True処理
        print("YES")
    else:
        #False処理
        print("NO")
> 
# [We Love Golf](https://atcoder.jp/contests/abc165/tasks/abc165_a)
2022/12/02 23:51
## Anwer
    a = int(input())
    b,c = map(int, input().split())

    exist = False


    for i in range(b,c+1):
        if i % a == 0:
            exist = True
            
    print("OK" if exist else "NG")
> 


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

# [Infinite Coins](https://atcoder.jp/contests/abc088/tasks/abc088_a)
2022/11/30 20:55
## Anwer
    a = [int(input()) for i in range(2)]
    b = (int(a[0]/500))

    if (a[0]-(b*500)) <= a[1]:
        print("Yes")
    else:
        print("No")
> 

# [B +/- A](https://atcoder.jp/contests/abc118/tasks/abc118_a)
2022/11/29 21:38
## Anwer
    a,b = map(int,input().split())

    if b % a ==0:
        print(a+b)
    else:
        print(b-a)
> 

# [Ferris Wheel](https://atcoder.jp/contests/abc127/tasks/abc127_a)
2022/11/28 23:19
## Anwer
    a,b = map(int, input().split())

    if a >= 13:
        print(b)
    elif a <= 12 and a > 5:
        print(b//2)
    elif a <= 5:
        print(0)
    else:
        print("error")
> ifによる複数分岐

# [+-x](https://atcoder.jp/contests/abc137/tasks/abc137_a)
2022/11/27 20:55
## Anwer
    a,b = map(int, input().split())
    c = a+b
    d = a-b
    e = a*b

    print(max(c,d,e))
> 

# [Serval vs Monster](https://atcoder.jp/contests/abc153/tasks/abc153_a)
2022/11/26 23:39
## Anwer
    a,b = map(int, input().split())

    if a % b ==0:
        print(a//b)
    else:
        print(a/b+1)
> 

# [Product](https://atcoder.jp/contests/abc086/tasks/abc086_a)
2022/11/25 22:42
## Anwer
    a,b = map(int, input().split())
    c = a*b
    if c % 2 == 0:
        print("Even")
    else
        print("Odd")
> ifによる分岐の表現
  
> 偶数と奇数を分ける際の適切な書き方

# [Multiplication 1](https://atcoder.jp/contests/abc169/tasks/abc169_a)
2022/11/24 23:30

## Answer
    a,b = map(int, input().split())
        print(a*b)
> 1行かつ複数の値を入力する
