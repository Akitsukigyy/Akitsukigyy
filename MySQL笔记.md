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

