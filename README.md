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
作业005：
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
            shuru


1. 写一个程序，判断给定年份是否为闰年。

year=input('请输入一个年份：')
while not year.isdigit():
    year = input("抱歉，您的输入有误，请输入一个整数：")
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

作业006：
0. 请写一个程序打印出 0~100 所有的奇数。
num=0
while num<101:
      if num % 2==0:
          
         print(num)
         num=num+1
      else:
          num=num+1
    
1.计算2的多少次方
num=int(input('想计算2的多少次方？请输入：'))
temp=1
while temp < (num+1):
      result=2**temp
      print(result)
      temp=temp+1


2.爱因斯坦曾出过这样一道有趣的数学题：有一个长阶梯，若每步上2阶，最后剩1阶；若每步上3阶，最后剩2阶；若每步上5阶，最后剩4阶；若每步上6阶，最后剩5阶；只有每步上7阶，最后刚好一阶也不剩。
我的原创代码：
temp=0
while (temp < 10000):
       temp=temp+1
       if  (temp%2==1)& (temp%3 ==2 )&(temp%5==4)&(temp%6==5)&(temp%7==0):
           print(temp)

作业007,008
0.按照 100 分制，90 分以上成绩为 A，80 到 90 为 B，60 到 80 为 C，60 以下为 D，写一个程序，当用户输入分数，自动转换为ABCD 的形式打印。
while 1:
    grade=input('请输入成绩(1-100)：')
    while not grade.isdigit():
        grade=input('输入非法，请输入一个整数：')
    grade=int(grade)
    if (90<=grade<101):
        print('成绩为A')
    elif (80<=grade<=90):
        print('成绩为B')
    elif  (60<=grade<80):
        print('成绩为C')
    elif  (grade<=60):
        print('成绩为D')
    else:
        print('输入的数值不在范围内！')
        
1.用三目操作符输出x,y,z中的最小值  
      
x=int(input('请为x赋值：'))
y=int(input('请为y赋值：'))
z=int(input('请为z赋值：'))
if x<y:
    small=x if x<z else z
else:
    small=y if y<z else z
print(small)    

member=['小童','小小童','童','小童最棒']
for i in member:
    print(i,len(i))

作业009：
0. 设计一个验证用户密码程序，用户只有三次机会输入错误，不过如果用户输入的内容中包含"*"则不计算在内。
code='小童最棒'
a=input('请输入密码:')
t=3
while 1:
       
    if (a == code)and (t>0): 
          print('密码正确，正在进入程序......')
          break
    elif '*'in a:
         b=str(t)
         print('密码中不能含有“*”号!您还有'+b+'次机会！')
         a=input('请输入密码:')    
    
    else:
           if t>1:
            print('密码错误！',end='')
            t=t-1
            c=str(t)
            print('您还有'+c+'次机会！')
            a=input('请输入密码:')
           else:

             print('密码错误，您没机会了！')
             break 
