- 👋 Hi, I’m @Akitsukigyy
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Akitsukigyy/Akitsukigyy is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->


列表
mylist = [a,b,c,d]
#清除列表中所有元素：mylist.clear()

#修改列表中特定下标索引的值：mylist[0]= 0

#指定下标中插入新元素：mylist.insert(1,"a") 其中1为插入位置，a为插入元素

#添加元素至列表尾部: mylist.append("b")

#添加一个新列表至原列表尾部： mylist2= [4,5,6,7],       mylist.extend(mylist2)

#del语句删除列表中的特定元素： del mylist[1]

#pop语句可去除元素： element = mylist.pop(2), mylist最终结果：[a,b,d], element:2

#删除某元素在列表中的第一个匹配项：mylist.remove(你要的项)

#数具体元素个数 mylist.count(你要数的元素)

#列表中的总元素个数： len(mylist)

#查找列表元素的下标位置： mylist.index(),若不存在会报错

#列表第一个元素 mylist[1], 最后一个元素: mylist[-1]

#列表的循环遍历：

#沿用mylist

#index = 0, while index < len(mylist):

#element = mylist[index]

#print(f"列表元素{mylist}")

#index += 1

元组
#元组内的内容无法修改，列表内的内容可以修改

#元组内若只有一个数据则需要加逗号，如 tuple("hello",)

#元组可以嵌套，如 tuple((1,2,3),(4,5,6))则元组内有两个元素， 若想取出元组内的元素“6”，则 num= tuple[1][2]

#由于其不可修改的特性，元组只有index, count, len等函数能够使用

#元组中嵌套list，则list可以修改

String字符串

#字符串可以使用replace函数进行修改， string.replace(old,new)，替换的逻辑为使用新的

#split函数对字符串进行切割，得到数个新的字符串，并存入列表中，字符串本身不变，得到了一个新的列表对象

#字符串以space分割，如 "1 2 3",则切割时使用space,如 split(" ") 记得要加双引号

#string.strip()去除前后空格， string.strip("12")去除前后12（1和2）

元组，字符串切片

#tuple = (1,2,3,4,5,6)， 切片包前不包后

#tuple[:] 对元组进行切片，从头切到位，所以直接：  ；步长为1，所以省略. 步长为2时，则为: tuple[::2]

#按照中括号顺序进行切片，tuple[1:2:2][1:2]

集合

#集合内重复的元素自动合并，无序，无法以下标定位

#set.add()添加

#set.pop()随机取出

#set.clear()清空集合

#set1={1,2,3}

#set2={3,4,5}

#set3=set1.difference(set2)

#set3={2,3} difference函数指取出set1中包含但set2中不包含的东西

#set3=set1.union(set2)合体

#由于集合不支持下标索引，所以无法使用while循环，但可以使用for循环

#容器排序， sorted(容器) sorted(容器，reverse=true)

#单引号比较字符ascii码大小，例如 'abc' > 'abd' 为 True


函数
#想返回多个值可以用多个变量去接受，如 x,y,z = def abc() return 1,2,3

#位置参数：传递参数时的个数和顺序必须一致，如 def function(1,2,3): print(f"{1}{2}{3},")

#关键字参数： def function(name, age, gender), print(f'your name is{}, ')

#函数嵌套: def function(compute): result = compute(1,2) print(...)

#需要再定义compute，有两种方法，一种普通定义，一种lambda定义。普通定义： def compute(a,b): return a+b ; lambda定义(其实不叫定义): 直接调用 function(lambda a,b:a+b)

#lambda函数为匿名函数，只能使用一次

文件

#f=open("文件名","r/a/w", encoding="UTF-8")

#content = f.read()  ; f.readlines("x行") or f.readline() readline表示读一行，readlines读全部

#close() 必须要close

#time.sleep(5000)

#with open("","","") as f: f readlines()   time.close()可以防止忘记close

# x=f.write() 会将写入内容保存至缓冲区

#x f.flush() 刷新，此时才将内容写进文档

#line.strip() strip函数去除行首尾指定字符，默认为空格或换行符

捕获异常
#try:     except Exception as e: print()   print(e)  else:  finally


模块  反复观看p95

两个.py文件可以调用互相的函数，这种行为就叫引入模块

main+tab 调出if --name-- = '--main--' 可以测试函数,在另一个.py导入时则只是导入而不会自动执行函数

all = [test.A] 则import*时只导入test A函数

pycharm中生成package自带init.py包，有这玩意才算个包，再在这个包上新建python file

import mypackage.module1后需要写mypackage.module1.info()

但如果 from mypakage.module import info 就只要写 info()

图表-折线图

from pyecharts.charts import Line #导入折线图
from pyecharts.options import TitleOpts，LegendOpts，ToolboxOpts,VisualMapOpts #导入图表选项,图例，工具箱,视觉映射

line = Line()                                       #存入变量

line.add_xaxis(["China", "America", "Britain"])    #设置x轴
line.add_yaxis("GDP",[30,40,50])                   #设置y轴，注意有标题GDP

line.set_global_opts(
    title_opts=TitleOpts(title="GDP show", pos_left="center",pos_bottom="1%")，
    legend_opt=LegendOpts(is show = True),
    toolbox_opts=ToolboxOpts(is_show=True)，
    visualmap_opts=VisualMapOpts(is_show=True)
    
)

#设置图标标题为gdp show, pos_left表示左移，center表示居中；pos_bottom=1%表示离开底部百分之1



line.render()                                      #生成图表

#更多配置选项参考 pyecharts.org中的全局配置项


数据处理实例：
import json
from pyecharts.charts import Line

f_us=open("D:\programming\pycharm\资料\资料\可视化案例数据\折线图数据\美国.txt","r",encoding="UTF-8")
us_data=f_us.read()
# 去除开头不规范字符

us_data=us_data.replace("jsonp_1629344292311_69436(","")
# 去除结尾不规范字符
us_data=us_data[:-2]

us_dict=json.loads(us_data)

print(type(us_dict))
print(us_dict)
# 获取trend key
trend_data=us_dict['data'][0]['trend']
# 获取x轴，取日期数据，至2020年12月31日，根据json网页显示data下标为313的日期为12月31日，切片时为314.多数据时，x轴公用，y轴不共用
us_x_data=trend_data['updateDate'][:314]
# 获取y轴
us_y_data=trend_data['list'][0]['data'][:314]


line=Line()

line.add_xaxis(us_x_data)

line.add_yaxis("美国确诊人数", us_y_data) #始终记得y轴要加注释

#生成图标，调用render方法
line.render()

f_us.close()

#is_piecewise=True，pieces=[{},{}] 是否分段，开启手动校准，匹配颜色

地图实例
from pyecharts.charts import Map
from pyecharts.options import VisualMapOpts
map = Map()

data=[
    ("上海市",99),
    ("北京市",199),
    ("湖北省",299),
    ("重庆市",399),
    ("台湾省",499)
]

map.add("测试地图",data,"china")

map.set_global_opts(
    visualmap_opts= VisualMapOpts(is_show=True,
                                  is_piecewise=True,
                                  pieces=[{"min":1,"max":9,"label":"1-9人", "color":"#CCFFFF"}])  #匹配颜色
)
map.render()

P106 实例，反复观看

实例失败:
import json
from pyecharts.charts import Map
from pyecharts.options import *

f = open("D:/programming/pycharm/资料/资料/可视化案例数据/地图数据/疫情.txt","r",encoding="UTF-8")
data=f.read()
# 读取后关闭文件
f.close()
# 取各个省份的数据并转换成python字典
data_dict=json.loads(data)
# 从字典中取出省份的数据
province_data_list=data_dict["areaTree"][0]["children"]
data_list=[]
for province_data in province_data_list:
    province_name = province_data["name"]
    province_confirm = province_data["total"]["confirm"]
    data_list.append((province_name,province_confirm))


###############################
# 以上为数据处理，接下来为制图
# 创建对象
map = Map()
# 添加数据
map.add("各省确诊人数", data_list,"china")
# 开始配置全局并定制分段的视觉映射
map.set_global_opts(
    title_opts=TitleOpts(title="全国疫情地图"),
    visualmap_opts = VisualMapOpts(
        is_show=True,           # 是否显示? True
        is_piecewise= True,     # 是否分段? True
        pieces=[
            {"min":1, "max":99, "label": "1-99人","color": "#CCFFFF"},
            {"min":100, "max":999, "label": "100-909人","color": "#FFFF99"},
            {"min":1000, "max":4999, "label": "1000-4999人","color": "#FF9966"},
            {"min":10000, "max":99999, "label": "10000-99999人","color": "#FF6666"},
            {"min":100000,  "label": "100000人以上","color": "#CC3333"}


        ]
    )
)

map.render("全国疫情地图.html")

#无法显示分段，不知为何，后期回来重做


柱状图则导入 bar

bar=Bar()

bar.add_xaxis()

#还可以加入 bar.reversal_axis() 反转xy轴，此时需要在y轴上把数据也带过来， label_opts=LabelOpts(position = "right")

添加时间线需要导入Timeline
实例：
from pyecharts.charts import Bar, Timeline
from pyecharts.options import LabelOpts
from pyecharts.globals import ThemeType # 给时间图表加入主题
# 构建bar1
bar1 = Bar()
bar1.add_xaxis(["中国","美国","英国"])
bar1.add_yaxis("GDP",[30,20,10],label_opts=LabelOpts("right"))
bar1.reversal_axis()

# 构建bar2
bar2 = Bar()
bar2.add_xaxis(["中国","美国","英国"])
bar2.add_yaxis("GDP",[40,25,15],label_opts=LabelOpts("right"))

bar2.reversal_axis()
# 构建bar3
bar3 = Bar()
bar3.add_xaxis(["中国","美国","英国"])
bar3.add_yaxis("GDP",[50,30,20],label_opts=LabelOpts("right"))

bar3.reversal_axis()

# 构建时间线对象
timeline=Timeline({"theme":ThemeType.DARK})  # 构建对象并赋予主题
# 时间线内添加时间线对象
timeline.add(bar1, "点位1")
timeline.add(bar2, "点位2")
timeline.add(bar3, "点位3")



# 自动播放设置
timeline.add_schema(
    play_interval= 1000,    # 播放间隔1000毫秒
    is_auto_play=True,      # 自动播放
    is_loop_play=True,      # 自动循环
    is_timeline_show=True   # 显示时间轴


)
# 绘图用时间线对象而不是bar对象
timeline.render("gdp时间线.html")




下面进行动态图的绘制，绘制前需要做一些准备，如拓展列表 sort：

my_list = [["a",33],["b",55],["c",11]]

def choose_sort_key(element):
    return element[1]

my_list.sort(key=choose_sort_key,reverse=True) # 注意不能带括号

# 默认排序从小到大，加上reverse就是从大到小

print(my_list)

lambda函数方法:
my_list = [["a",33],["b",55],["c",11]]
my_list.sort(key=lambda element:element[1], reverse=True)
print()

P110 反复观看

构建对象：

class student:
    name = None

    def say_hi(self):     # class中的函数就是方法了，定义方法时会自动加self
        print(f"名字为{self.name}")    # 调用类内部的参数时要加self.

stu = student()
stu.name="Aki"
stu.say_hi()              # 不用加self

#想要访问成员属性，必须要加 self.xxx

class student:
    name = None

    def say_hi(self):
        print(f"名字为{self.name}")
    
    def say_hi2(self,msg):
        print(f"{self.name},{msg}")

stu = student()
stu.name="Aki"
stu.say_hi()
stu.say_hi2("nice!")

# 定义sayhi2时，注意括号内的内容， def xxx(self,变量1，变量2，变量3)，则调用时会出现不同，如 stu.say_hi2("变量1"，“变量2”)， self自动填充

import winsound    winsound.Beep("频率","持续时间")可以让电脑发出小声音，不建议尝试


def _init_(self,name,age,tel):
    self.name=
    self.age=
    self.tel=
    print("Student")

stu=student("name",31,"tel")

例：

class Student:
    name = None     # 可省略
    age = None      # 可省略
    tel = None      # 可省略

    def __init__(self,name,age,tel):
        self.name = name    # 赋值+定义
        self.age = age
        self.tel = tel
        print("Student类创建对象")

stu = Student("Aki",27,"18217523297")
print(stu.tel)
print(stu.age)
print(stu.name)


super()表示调用父类对象,可以调用已经被复写的对象
super().父类()

变量

变量注解：

Var_1: int = 15

my_list: list[int] = [1,2,3]   #最佳表达方法
my_dict: dict[str,int] = {"number": 11}

alt+enter 可以搜索可导包

def add(a:int,b:int):
    return x+y           # 可以让pycharm了解你想要做什么 从而
    
def func(data:list) -> list:       ->list为对func的注解

my_list:list[Union[str,int]] = [1,2,"abc"] # Union 可以对多种数据结构进行注解

P124多看几遍

P124 具体案例查看.py


conf = SparkConf().setMaster("local[*]").setAppName("test_spark_app")

上下属于一个效果

conf = SparkConf()
conf.setMaster("local[*]")
conf..setAppName("test_spark_app")


pyspark-map 方法

from pyspark import SparkConf, SparkContext
import os
os.environ['PYSPARK_PYTHON'] = "D:/programming/pycharm/python/python.exe"    # 这一步帮助pyspark找到python解释器的位置，environ 表示environment环境变量

完整map方法示例:

from pyspark import SparkConf, SparkContext
import os
os.environ['PYSPARK_PYTHON'] = "D:/programming/pycharm/python/python.exe"
# 创建SparkConf类对象
# setMaster设置运行模式，setAppName设置人物名称
conf = SparkConf().setMaster("local[*]").setAppName("test_spark_app")
# 基于SparkConf类对象创建SparkContext对象

sc = SparkContext(conf = conf)

# 打印pyspark运行版本

print(sc.version)

# 停止sparkcontext对象的运行（停止pyspark程序）
# sc.stop()

# 准备RDD
rdd = sc.parallelize([1,2,3,4,5])
# 通过map方法将所有数据乘以10
def func(data):
    return data * 10
rdd2 = rdd.map(func)   # 也可以直接（lambda：x:X*10） 然后将前面的def注释掉

print(rdd2.collect())

结果得到 10-50
 map 方法就是将 sc.parallelize[1-5]中的1-5传递给 rdd2 = rdd.map(func),具体func自己定义  # 对rdd内的元素进行逐个处理产生新的rdd
 
 链式函数：
 rdd.map().map().map()
 
 flatmap和map非常相似，但多了个接触嵌套的功能 [[]123],[123],[123]] 变为[123,123,123]
 
 
 例如：
 rdd = sc.parallelized(["itheima,itcast,666","itheima1,itheima2,itheima3","itheima4,itheima5,itheima6 "])
 rdd2 = rdd.map(lambda x:x.split(" "))    map会报错，flatmap不会
 
 print后全部拆出来，"itheima","itcast","666"
 
 
 KV型RDD， 指二元元组   KV - Key Value 
 对应 [('a',1),('b',2),('c',3)]
 
 例子：
 # 准备rdd

rdd3 = sc.parallelize([('男',99),('男',88),('女',99),('女',66)])

# 求男生女生两组的成绩之和
rdd4 = rdd3.reduceByKey(lambda a,b: a + b)
print(rdd4.collect())

得到
[('男', 187), ('女', 165)]

P145 案例再看

rdd.map(lambda word:(word,1))  可以将'it' 变为 （'it',1）


filter 方法取 true，舍弃false
例子：
rdd = sc.parallelize([1,2,3,4,5])
rdd.filter(lambda x:True if(x % 2 == 1) else False)
得到 [2,4]

distinct 方法去重
rdd.distinct() 无需传参
直接print(rdd.distinct().collect())即可

rdd.saveAsTextFile("D:/output1") #  在配置完hadoop后，即可写入文档
os.environ['HADOOP_HOME'] = 'D:\programming\pycharm\资料(1)\第15章资料\资料\hadoop-3.0.0.tar\hadoop-3.0.0\hadoop-3.0.0'

存储后的文件根据电脑的核心数可能会分成16个区，可用以下方法变为1个区
# 方法1: SparkConf对象设置属性全局并行度为1
conf = SparkConf().setMaster('local[*]').setAppName("test_spark")
conf.set('spark.default.parallelism","1")
sc = SparkContext(conf=conf)

# 方法2，创建RDD的时候设置（parallelize方法传入numSlices参数为1）
rdd1 = sc.parallelize([1,2,3,4,5], numSlices = 1))
rdd1 = sc.parallelize([1,2,3,4,5],1)


综合案例:
# 打印输出：热门搜索时间段Top3
# 打印输出：热门搜索词Top3
# 打印输出：统计黑马程序员关键字在那个时间段被搜索最多
# 将数据转换为JSON格式，写出为文件

import os
from pyspark import *
os.environ['PYSPARK_PYTHON'] = 'D:/programming/pycharm/python/python.exe'
os.environ['HADOOP_HOME'] = 'D:/programming/pycharm/资料(1)/第15章资料/资料/hadoop-3.0.0.tar/hadoop-3.0.0/hadoop-3.0.0'
conf = SparkConf().setMaster("local[*]").setAppName("test_spark")

# 分成一个区
conf.set("spark.default.parallelism","1")

sc = SparkContext(conf=conf)

# 读取文件转换成RDD
file_rdd = sc.textFile("D:/programming/pycharm/资料(1)/第15章资料/资料/search_log.txt")
# TODO 需求1：热门搜索时间段Top3（小时精度）
# 1.1 去除全部的时间并转换为小时
# 1.2 转换为（小时，1）的二元元组
# 1.3 Key分组聚合Value
# 1.4 排序（降序）
# 1.5 取前三
result1 = file_rdd.map(lambda x: x.split("\t")).\
    map(lambda x: x[0][:2]).\
    map(lambda x: (x, 1)).\
    reduceByKey(lambda a, b: a+b).\
    sortBy(lambda x: x[1], ascending=False, numPartitions=1).\
    take(3)
# 这三个map可以写为： (lambda x: x.split("\t")[0][:2]),1)
print("需求1的结果为：", result1)

# TODO 需求2： 热门搜索词Top3
# 2.1 去除全部的搜索词
# 2.2（词，1）二元元组
# 2.3 分组聚合
# 2.4 排序
# 2.5 Top3
result2 = file_rdd.map(lambda  x: (x.split("\t")[2],1)).\
    reduceByKey(lambda a,b: a + b).\
    sortBy(lambda x: x[1],ascending=False,numPartitions=1).\
    take(3)

print("需求2的结果为：", result2)

# TODO 需求3：统计黑马程序员关键字在什么时段被搜索最多
# 3.1 过滤内容，只保留黑马程序员关键词
# 3.2 转换为（小时，1）的二元元组
# 3.3 Key分组聚合Value
# 3.4 排序（降序）
# 3.5 取前1
result3 = file_rdd.map(lambda x: x.split("\t")).\
    filter(lambda x: x[2] =='黑马程序员').\
    map(lambda x:(x[0][:2],1)).\
    reduceByKey(lambda a,b: a + b).\
    sortBy(lambda x:x[1],ascending=False,numPartitions=1).\
    take(1)
print("需求3结果为：",result3)


# TODO 需求4： 将数据转换为JSOM格式，写出到文件中
# 4.1 转换为JSON格式的RDD
# 4.2 写出为文件

file_rdd.map(lambda x:x.split("\t")).\
    map(lambda x:{"time": x[0],"user_id":x[1],"key_word":x[2],"rank1":x[3],"rank2":x[4],"url":x[5]}).\
    saveAsTextFile("D/output_json")
    
    
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
text="only YOU Loving yoU,你是我的唯一，jUst YoU,我能等你下课吗？能不能一起去逛街？达能小王子"
 
#大小写转换
text.upper() #大写
text.lower() #小写
text.title()#首字母大写
text.capitalize()#第一个字母大写
text.swapcase()#大小写对调
 
#字符串的搜索
text.count("o")#搜索并统计"o"出现的次数
text.count("o",28)#搜索并统计，从第28位开始，"o"出现的次数
text.startswith("only")#text以"only"开通
text.startswith("only",2,10)#text的第3-9个字符以"only"开通
text.find("you")#查找you
text.replace("u","V",2)
 
#填充或者剔除某些信息
 
"1999".rjust(10,"$")#前一个字符代表填充后字符串的总长度
"1999".rjust(5,"$")
"1999".zfill(9)#用0填充，类似 "1999".rjust(9,"0")
"1999".rjust(9,"0")
"1999".center(50) #在左右两边都假设空格
"   1999   ".strip()#去重左右两边的空格
"1999".strip("9")#去重左右两边的"9"
" 1999 ".strip("9")#去重左右两边的"9",两边是空格没有9
 
#字符串的分割与合并
 
text.replace("能",",")
text1=text.replace("能","\n")
print(text1)
print(text.replace("能","\n"))
text.split("能")#以"能"为结点把str拆成一个字列表
text.partition("能") #以"能"为结点把str拆成一个字元组
text.rpartition("能")
text1.splitlines()#识别空行进行分割
text1.split("\n")#同上分割空行
"@".join(text)#把@插入到str的每一个字符中
"12345".join("  ")#重复并拼接


