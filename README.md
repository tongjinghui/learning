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
             
1. 编写一个程序，求 100~999 之间的所有水仙花数。
num=100
while num<1000:
    a=num%10
    b=num//10
    c=b%10
    d=b//10
    if num==(a**3+c**3+d**3):
        print(num)
    num=num+1
    
2.   有红、黄、蓝三种颜色的求，其中红球 3 个，黄球 3 个，绿球 6 个。先将这 12 个球混合放在一个盒子中，从中任意摸出 8 个球，编程计算摸出球的各种颜色搭配。 
print('red\tyellow\tgreen')
for red in range(0,4):
    for yellow in range(0,4):
        for green in range(2,7):
            if red+yellow+green==8:
                print(red,'\t',yellow,'\t',green)

作业010
0. 自己动手试试看，并分析在这种情况下，向列表添加数据应当采用哪种方法比较好？

假设给定以下列表：

member = ['小甲鱼', '黑夜', '迷途', '怡静', '秋舞斜阳']

要求将列表修改为：

member = ['小甲鱼', 88, '黑夜', 90, '迷途', 85, '怡静', 90, '秋舞斜阳', 88]

member=['小甲鱼','黑夜','迷途','怡景','秋舞斜阳']
member1=['小甲鱼',88,'黑夜',90,'迷途',85,'怡景',90,'秋舞斜阳',88]
member.insert(1,88)
member.insert(3,90)
member.insert(5,85)
member.insert(7,90)
member.insert(9,88)
print(member1)
print(member)

1. 利用 for 循环打印上边 member 列表中的每个内容
 for each  in member:
    print(each )
    
2. 上一题打印的样式不是很好，能不能修改一下代码打印成下图的样式呢？【请至少使用两种方法实现】
member=['小甲鱼',88,'黑夜',90,'迷途',85,'怡景',90,'秋舞斜阳',88]
count=0
while count<len(member):
    if count%2==0:
        print(member[count],member[count+1])
        count=count+2

for each in range(len(member)):
    if each%2==0:
        print(member[each],member[each+1])

作业012：
1 问题：请先在 IDLE 中获得下边列表的结果，并按照上方例子把列表推导式还原出来。
list1=[]
for x in range(10):
    for y in range(10):
        if (x%2==0)and(y%2!=0):
            
                list1.append((x,y))
print(list1)            

2.请使用列表推导式补充被小甲鱼不小心涂掉的部分
list1=['1.Just do it','2.一切皆有可能','3.让编程改变世界','4.Impossible is Nothing']
list2=['4.阿迪达斯','2.李宁','3.鱼c','1.耐克']
list3=[name+':'+slogan[2:] for name in list2 for slogan in list1 if slogan[0]==name[0]]
list3.sort
for each in list3:
    print(each)
number = '0123456789'
zimu = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'
fuhao = r'''~!@$%^&*()_=-/,.?<>;:[]{}|\#'''

# 密码安全性检查代码
#
# 低级密码要求：
#   1. 密码由单纯的数字或字母组成
#   2. 密码长度小于等于8位
#
# 中级密码要求：
#   1. 密码必须由数字、字母或特殊字符（仅限：~!@#$%^&*()_=-/,.?<>;:[]{}|\）任意两种组合
#   2. 密码长度不能低于8位
#
# 高级密码要求：
#   1. 密码必须由数字、字母及特殊字符（仅限：~!@#$%^&*()_=-/,.?<>;:[]{}|\）三种组合
#   2. 密码只能由字母开头
#   3. 密码长度不能低于16位

code=input('请输入需要检查的密码组合：')

length=len(code)

while(' 'in code)or (length==0):
    print('密码不能为空或含有空格！')
    code=input('请重新输入需要检查的密码组合：')
    
    length=len(code)

if 0<length<=8:
    lg=1
elif 8<length<=16:
    lg=2
else:
    lg=3

shului=0
for each in code:
    if each in number:
        shului=shului+1
        break
    
for each in code:
    if each in zimu:
        
        shului=shului+1
        break
    
for each in code:
    if each in fuhao:
        
        shului=shului+1
        break
    
while (1):

    if (shului==3)and (lg == 3 )and(code[0] in zimu):
        print('您的密码安全级别评定为：高\n请继续保持')
        
        break
    else:
        if (shului>=2)and (lg>=2):
               print('您的密码安全级别评定为：中')
        else :
           print('您的密码安全级别评定为：低')
    
       
    print('请按以下方式提升密码安全级别：')
    print('1.密码必须由数字，字母及特殊字符三种组合')
    print('2.密码只能由字母开头')
    print('3.密码长度不低于16位')
    break

作业015：

0.编写一个进制转换程序
while (1):
    num=input('请输入一个整数(输入Q结束程序)：')
    if num=='Q':
        break
    while ( num.isdigit() is False):
        num=input('输入有误，请重新输入一个整数(输入Q结束程序)：')
        if num=='Q':
            break
    if num=='Q':
            break    
    num=int(num)
    x='%x' % num
    o='%o' % num
    d=bin(num)
    num=str(num)
    x=str(x)
    o=str(o)
    d=str(d)
    print('十进制 -> 十六进制：'+ num +' -> 0x'+ x)
    print('十进制 ->   八进制：'+ num +' -> 0o'+ o)
    print('十进制 ->   二进制：'+ num +' -> '+ d)

作业016：
0.补全代码
name =  input('请输入待查找的用户名：')
score = [['迷途',85],['黑夜',80],['小布丁',65],['福娃',95],['怡景',90]]
IsFind = False

for each in score:
    if name in each:
        print(name+'的得分是：',each[1])
        IsFind = True
        break
    
if IsFind == False:
    print('找不到！')

1.猜想一下 min() 这个BIF的实现过程
name =  input('请输入一串数字：')
min1=name[0]

#name = int (name)
for each in name:
    if each < min1 :
        min1=each
print(min1)

2. 视频中我们说 sum() 这个BIF有个缺陷，就是如果参数里有字符串类型的话就会报错，请写出一个新的实现过程，自动“无视”参数里的字符串并返回正确的计算结果
num='0123456789'
sum1=0
code=input('请输入一串数字：')
for each in code:
    if each not in num:
       code.replace(each,'0')
    else:   
        each=int(each)    
        sum1=sum1+each
print(sum1)

作业017：
0. 编写一个函数 power() 模拟内建函数 pow()，即 power(x, y) 为计算并返回 x 的 y 次幂的值。

def power(x,y):
    return print(x**y)
