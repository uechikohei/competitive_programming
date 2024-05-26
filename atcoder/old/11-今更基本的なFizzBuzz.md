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