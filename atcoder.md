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