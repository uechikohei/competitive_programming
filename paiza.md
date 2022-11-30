

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