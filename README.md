# learning
20210416
作业002：
0. 编写程序：hello.py，要求用户输入姓名并打印“你好，姓名！”
name = input("请输入您的姓名：")
print('你好，' + name + '!')

1. 编写程序：calc.py 要求用户输入1到100之间数字并判断，输入符合要求打印“你妹好漂亮”，不符合要求则打印“你大爷好丑”
temp = input("请输入1到100之间的数字：")
num = int(temp)
if 1 <= num <= 100:
    print('小童最棒')
else:
    print('小童一定会变强的')

作业003：
0.使用变量，计算一年有多少秒？

提示：可以以 DaysPerYear（每年天数），HoursPerDay（每天小时数），MinutesPerHour（每小时分钟数），SecondsPerMinute（每分钟秒数）为变量名。
DaysPerYear = 365
HoursPerDay = 24
MinutesPerHour = 60
SecondsPerMinute = 60
result = DaysPerYear * HoursPerDay * MinutesPerHour * SecondsPerMinute
print(result)

作业004：
1. 尝试写代码实现以下截图功能：
temp = input('请输入一个整数:')
number = int(temp)
i = 1
while number:
    print(i)
    i = i + 1
    number = number - 1
    
  2. 尝试写代码实现以下截图功能： 
 temp=int(input('请输入一个整数:'))

while temp:
      print(' '*temp+'*'*temp)
      temp=temp-1

20210417
改进版猜数字小游戏2.0

import random
secret=random.randint (1,100)
print('............改进版猜数字小游戏2.0............')
times=int(input('你想猜几次？'))
guess=int(input('猜猜小童现在在想哪个数字（1—100）：'))
t=times

while (1):
        
        if guess>secret:
           print('猜大了喔')
           t = t-1
           if t>0:
               guess=int(input('再猜一次吧：'))
           else:
               b=str(times)
               c=str(secret)
               print(b+'次机会用完了，游戏结束')
               print('很遗憾你没有猜中，小童心里想的是'+c+'喔\n下次记得多给自己一些机会吧!')
               break
        elif guess<secret: 
             print('猜小了喔')
             
             t=t-1
             if t>0:
               guess=int(input('再猜一次吧：'))
             else:
               d=str(times)
               e=str(secret)
               print(d+'次机会用完了，游戏结束')
               print('很遗憾你没有猜中，小童心里想的是'+e+'喔\n下次记得多给自己一些机会吧!')
               break
        else :
            a=str(times - t+1)
            f=str(secret)
            print('真棒,你猜对了！小童心里想的就是'+f+'喔，你一共猜了'+a+'次！')
            break


1. 写一个程序，判断给定年份是否为闰年。

year=input('请输入一个年份：')
while not year.isdigit():
    temp = input("抱歉，您的输入有误，请输入一个整数：")
year=int(year)    
if  year%400==0:
    year=str(year)
    print(year+'是闰年')
else :
    if  (year%4==0)and(year%100!=0):
        year=str(year)
        print(year+'是闰年')
    else:
        year=str(year) 
        print(year+'不是闰年')
    
0. 请写一个程序打印出 0~100 所有的奇数。
num=0
while num<101:
      if num % 2==0:
          
         print(num)
         num=num+1
      else:
          num=num+1
    



