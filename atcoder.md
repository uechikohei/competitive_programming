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