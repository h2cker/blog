**Python学习笔记**


``print("hello") #输出使用print

name = "Mythacker is"
print(name.title()) #.title()首字母大写
print(name.upper()) #.upper()全部大写
print(name.lower()) #.lower()全部小写

#合并字符串
first_name = "my"
last_name = "thacker"
full_name = first_name + "" +last_name
print(full_name)
print(full_name.title()) #首字母大写

#制表符\t  换行符\n
print("Python")
print("\tPython")
print("hello\nPython")

#删除字符串空白
del_str = "Python 1 "
print(del_str)
print(del_str.rstrip())

#str类型错误
age = 23
age_message = "Happy " + str(age) +"rd Birthday!"
print(age_message)

#列表
list_name = ['a','b','c','d']
print(list_name)
print(list_name[0])
print(list_name[0].title()) #大写
print(list_name[-1])
print(list_name[-2])

list_name[0] = "aa"
print(list_name[0]) #修改列表元素
print(list_name)

list_name.append('e')
print(list_name) #添加列表元素.append()

list_name.insert(0,'aaa')
print(list_name) #插入列表元素.insert(索引,'值')

del list_name[0] #删除元素 删除指定索引的元素
print(list_name)

poped_list_name = list_name.pop()
print(list_name) #弹出一个元素.pop()
#如果你要删除一个元素，且不再以任何方式使用它，就使用del删除元素；如果你要在删除元素后还能继续使用它，就使用pop方法

list_name.remove('c')
print(list_name) #根据值来删除元素.remove()

#组织列表
cars = ['bwm','audi','toyota','subaru']
cars.sort() #使用sort()对列表进行永久排序
print(cars)
cars_lens = len(cars)
print(cars_lens) #len()确定长度

#遍历
magic_name = ['aaa','bbb','ccc']
for magic in magic_name:
	#print(magic)
	print(magic.title() + ",is " +magic.title())
	print("see you " + magic.title() + "\n")
print("Thank you")

#创建数字列表  range()
for value in range(1,5):
	print(value)

number = list(range(1,6))
print(number)

even_number = list(range(2,11,2))
print(even_number) #指定步数

squares = []
for value in range(1,11):
	squares.append(value**2)
print(squares) 
``
