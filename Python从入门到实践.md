# **python 从入门到实践**

1. 变量和数据类型

   1. 变量：

      ​	非关键字，字母数字和下划线组成 字母下划线打头 避免使用小写l和o,和大写字母

   2. 简单数据类型

      - 字符串：
        - ​	单双引号都可构成字符串 
        - 使用方法对字符串进行操作
        - 修改字符串大小写  .title() 以首字母大写的方式显示每个单词 .upper .lower()字符串改为全部大写或全部小写

      - ```python
        name = "ada lovelace" 
        print(name.title())   
        Ada Lovelace`
        
        name = "Ada Lovelace" 
        print(name.upper())
      print(name.lower())   
        ADA LOVELACE 
      ada lovelace` 
        ```

        

        - 合并（拼接字符串）：Python使用加号（+）来合并字符串

        - Python能够发现'python '中额外的空 白，并认为它是有意义的——除非你告诉它不是这样的  所以对字符串中的空白字符进行删除是十分必要的

           lstrip()：删除字符串首的空白并返回值；strip()删除字符串两端的空白并返回值
        
           rstrip():删除字符串尾的空白并返回值，通过将返回值重新赋给变量实现删除空白
        
        ```python
      `print("Languages:\nPython\nC\nJavaScript") Languages: Python C JavaScript`
        

        ```
        
        
        
      - 数字:整数和看浮点数，加减乘除

      - 注释：# 添加注释多行注释使用三引号

   3. 基本数据类型

      - 列表：列表由一系列按特定顺序排列的元素组成。

      - 用方括号（[]）来表示列表，并用逗号来分隔其中的元素。

      - ```python
        `bicycles = ['trek', 'cannondale', 'redline', 'specialized'] print(bicycles)` 
        ```

      - 列表是有序集合，因此要访问列表的任何元素，只需将该元素的位置或索引告诉Python即可。Python为访问最后一个列表元素提供了一种特殊语法。通过将索引指定为-1，可让Python返 回最后一个列表元素：

      - **列表元素的操作：**

        - 修改列表元素：可指定列表名和要修改 的元素的索引，再指定该元素的新值。

          - `motorcycles = ['honda', 'yamaha', 'suzuki']  motorcycles[0] = 'ducati'` 

        - 添加列表元素：分为在列表尾添加元素和在列表中插入元素

          - 在表尾添加元素：使用方法append() 在表尾添加元素

            - ```python
              #调用append方法可以创建一个空的的列表实现动态插入
              motorcycles = [] motorcycles.append('honda') motorcycles.append('yamaha') motorcycles.append('suzuki') print(motorcycl]]][es)
              ```

          - 在表中插入元素：使用方法insert()可在列表的任何位置添加新元素。为此，你需要指定新元素的索引和值。

          - ```python
            motorcycles = ['honda', 'yamaha', 'suzuki']
            motorcycles.insert(0, 'ducati') 
            ```

        - 删除列表元素：

          - 根据位置删除：如果知道要删除的元素在列表中的位置，可使用del语句。

            ```python
            motorcycles = ['honda', 'yamaha', 'suzuki']
            
            print(motorcycles) 
            
            del motorcycles[0] 
            
            print(motorcycles)
            
            ---['honda', 'yamaha', 'suzuki'] 
            ‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘’‘
            ---['yamaha', 'suzuki'] 
            ```

          - 删除并使用删除元素的值:**方法pop()删除列表末尾的元素**，并让你能够接着使用它。只要在括号内加入索引值，就能删除任意位置的元素

            ```python
            motorcycles = ['honda', 'yamaha', 'suzuki']
            
            print(motorcycles)
            
            popped_motorcycle = motorcycles.pop() 
            
            print(motorcycles) 
            
            print(popped_motorcycle) 
            
            ---['honda', 'yamaha', 'suzuki'] 
            
            ---['honda', 'yamaha'] 
            
            ---suzuki 
            ```

          - 根据值删除：你只知道要删除的元素的值，可使 用方法remove()。

          - ```python
            motorcycles = ['honda', 'yamaha', 'suzuki', 'ducati'] print(motorcycles) motorcycles.remove('ducati') print(motorcycles)
            ```

        - 对列表进行排序

          - 永久性排序：使用.sort()方法对列表惊醒字母排序，你还可以按与字母顺序相反的顺序排列列表元素，为此，只需向sort()方法传递参数 reverse=True。

            - ```python
              cars.sort(reverse=True) print(cars) 
              ```

          - 临时排序:要保留列表元素原来的排列顺序，同时以特定的顺序呈现它们，可使用函数sorted()。函数 sorted()让你能够按特定顺序显示列表元素，同时不影响它们在列表中的原始排列顺序。

            ```python
            print("\nHere is the sorted list:") print(sorted(cars))
            ```

          - 颠倒列表：要反转列表元素的排列顺序，可使用方法reverse()，反转列表元素

          - 列表长度：使用函数len()可快速获悉列表的长度。

            ```python
             cars = ['bmw', 'audi', 'toyota', 'subaru'] 
             len(cars) 
             ---4 
            ```

        - 创建数值列表：

          - 使用range()函数生成一系列数字；

          - 使用函数list()将range()的结果直接转换为列表，使用函数range()时，还可指定步长

            ```python
            numbers = list(range(1,6)) 
            print(numbers)
            [1, 2, 3, 4, 5] 
            even_numbers = list(range(2,11,2))
            print(even_numbers)
            [2, 4, 6, 8, 10] 
            
            ```

          - 列表解析：定一个描述性的列表名，如squares；然后，指定一个左方括号， 并定义一个表达式，用于生成你要存储到列表中的值。在这个示例中，表达式为value**2，它计 算平方值。接下来，编写一个for循环，用于给表达式提供值，再加上右方括号。

            ```python
            squares =[value **2 for value in range(1,11)]
            
            print(squares)
            ```

        - 列表切片：

          ```python
          players = ['charles', 'martina', 'michael', 'florence', 'eli'] 	print(players[0:3]) 
          ['charles', 'martina', 'michael']
          #遍历切片
          players = ['charles', 'martina', 'michael', 'florence', 'eli']
          print("Here are the first three players on my team:")
          for player in players[:3]:
           	print(player.title()) 
          Here are the first three players on my team:
          Charles
          Martina
          Michael 
          
          ```

        - 列表复制：要复制列表，可创建一个包含整个列表的切片，方法是同时省略起始索引和终止索引（[:]）。

          ```python
          #创建一个列表的副本
          my_foods = ['pizza', 'falafel', 'carrot cake'] 
          
          friend_foods = my_foods[:] 
          
          print("My favorite foods are:") 
          
          print(my_foods) print("\nMy friend's favorite foods are:") 
          
          print(friend_foods) 
          
          My favorite foods are: ['pizza', 'falafel', 'carrot cake']
          
          My friend's favorite foods are: ['pizza', 'falafel', 'carrot cake']
          #这是将列表名赋给了另一个变量，两者指向同一个列表
           friend_foods = my_foods
          
          ```
      
        - 在列表中移动元素

        - ```python
          #进行客户验证“
          unconfirmed_users = ['anda','mike','jerry']
          confirmed_users=[]
          while unconfirmed_users:
              user = unconfirmed_users.pop()
              print("confirmed_user is "+user.title())
           confirmed_users.append(user)
          print("confirm complete!!!")
       for confirmed_user in confirmed_users:
              print(confirmed_user + ' '+"is confirmed")
          ```
       ```
      
       
      
      - 元组：不可变的列表
      
        ```python
        dimensions = (200, 50) 
        print(dimensions[0]) 
        print(dimensions[1]) 
        200
        50
       ```
      
   
     元组中的元素不可改变；但是可以通过给整个元组进行重新赋值，进行修改
   
   - 字典：在Python中，字典是一系列键—值对。每个键都与一个值相关联，你可以使用键来访问与之 相关联的值。与键相关联的值可以是数字、字符串、列表乃至字典。事实上，可将任何Python对 象用作字典中的值。
     
        *注意，键—值对的排列顺序与添加顺序不同。Python不关心键—值对的添加顺序， 而只关心键和值之间的关联关系。*
      
        ```python
        #在python中定义空白字典，在依次添加
        alien_0 = {'color': 'green', 'points': 5}
        print(alien_0)
        alien_0['x_position'] = 0
        alien_0['y_position'] = 25
        print(alien_0)
        
       --->{'color': 'green', 'points': 5}
        --->{'color': 'green', 'points': 5, 'y_position':25,'x_position': 0}
        
       ```
     ```
      
        - 字典的循环结构：要编写用于遍历字典的for循环，可声明两个变量，用于存储键—值对中的键和值。 对于这两个变量，可使用任何名称。Python不关心键—值对的存 储顺序，而只跟踪键和值之间的关联关系。
      
          ```python
          #一种遍历的演示效果
          favorite_languages = {
           'jen'   : 'python',
           'sarah' : 'c',
           'edward': 'ruby',
           'phil'  : 'python',
           }
          for name, language in favorite_languages.items():
          print(name.title() + "'s favorite language is "+language.title() + ".")
     ```
  ```
   
        - 使用.keys方法只获取字典的名称，使用.value()方法获取字典的值；通过对包含重复元素的列表调用set()，可让Python找出列表中独一无二的元素
          
        - ```python
          #输出字典中的独立的键和值
          favorite_languages = {
           'jen': 'python',
           'sarah': 'c',
           'edward': 'ruby',
           'phil': 'python',
           }
          
          #单独输出键值
          for name in favorite_languages.keys():
              print(name)
         print("\n")
          #单独输出值
         for value in favorite_languages.values():
              print(value)
          print("\n")
          #单独输出排序的键值
          for name in sorted(favorite_languages.keys()):
              print(name)
          print("\n")
          #单独输出排序的值
          for Language in sorted(favorite_languages.values()):
              print(Language)
          print("\n")
          #单独输出不重复的值
          for Language in sorted(set(favorite_languages.values())):
              print(Language)
  ```

        - 嵌套：将一系列字典存储在列表中，或将列表作为值存储在字典中，进行相互嵌套
          
          ```python
          #将字典嵌套在字典中
          users = {
           'aeinstein': {
           'first': 'albert',
           'last': 'einstein',
           'location': 'princeton',
           },
           'mcurie': {
           'first': 'marie',
           'last': 'curie',
           'location': 'paris',
           },
           }
          for username, user_info in users.items():
          	print("\nUsername: " + username)
          	full_name = user_info['first'] + " " + user_info['last']
          	location = user_info['location']
          	print("\tFull name: " + full_name.title())
          	print("\tLocation: " + location.title())
          #将列表嵌套在字典中：
          users = {'nancy':['python','java'],
                    'jack':['python'],
                    'hank':['c','java','python']}
          for name,languages in users.items():
              print(name.title())
              for language in languages:
                  print("\t"+language)
          #Python 字典(Dictionary) items() 函数以列表返回可遍历的(键, 值) 元组数组。/t是打印一个制表符
          ```


   ​       

2. 条件结构和循环结构

   1. 条件结构：if语句；and连接多个判断条件；or表示或

      - if-else语句；if-elif-else

   2. 循环结构：

      - for循环：

        ```python
                                magicians = ['alice', 'david', 'carolina'] 
        
                 				for magician in magicians: 
        
                ​						print(magician)
        
                ​				-------alice 
        
                ​				-------david
        
                ​				-------carolina
        ```
        
      - while循环：
      
        while循环时执行到条件不满足为止
      
        ```python
        current_number = 1
        while current_number <= 5:
        print(current_number)
        current_number += 1
        #调查报告存储
        responses = {}
        flag = "True"
        while flag:
            name = input("What's your name ? \n")
            response = input("What's your favorite food ?\n")
            responses[name] = response
            
            judgement = input("你愿意参与吗？\n")
            if judgement == "no":
                break
        for name,food in responses.items():
            print(name+"would like to eat"+response)
        ```
      
        

3. 函数:

   - ```python
      def greet_user():
     """显示简单的问候语"""
     print("Hello!")
     greet_user()
     ```

     

   - 用户输入函数：input()函数，将用户输入的文本存在变量中，

4. 类：

   - **类是一类事物的通用性定义；根据类创建对象被称为实例化**

   - ***_init__()**是一个特殊的方法，每当你根据Dog类创建新实*
     *例时，Python都会自动运行它。在这个方法的名称中，开头和末尾各有**两个下划线**，这是一种约定，旨在避免Python默认方法与普通方法发生名称冲突。*

   - *我们将方法__init__()定义成了包含三个形参：self、name和age。在这个方法的定义中，形
     参self必不可少，还必须位于其他形参的前面。属性也可以直接赋值，倘若调用时未对属性进行再次赋值，则将使用默认值。Python调用这个__init__()方法来创建Dog实例时，将自动传入实参self。每个与类相关联的方法
     调用都自动传递实参self，它是一个指向实例本身的引用，让实例能够访问类中的属性和方法。
     我们创建Dog实例时，Python将调用Dog类的方法__init__()。我们将通过实参向Dog()传递名字和年龄；self会自动传递，因此我们不需要传递它。*

   - **同一个类可以同时创建多个对象**

   - **在定义类时可以创建一个初始属性默认，不用输入，直接调用**

   - **修改属性值的方法**：1.直接在调用时重新赋值   2.通过定义方法，调用方法对属性进行重新修改

   - **继承**：*一个类继承另一个类时，它将自动获得另一个类的所有属性和方法。首先是Car类的代码。创建子类时，父类必须包含在当前文件中，且位于子类前面。*
     *我们定义了子类ElectricCar。定义子类时，必须在括号内指定父类的名称。方法__init__()*
     *接受创建Car实例所需的信息。*
     *super()是一个特殊函数，帮助Python将父类和子类关联起来。这行代码让Python调用*
     *ElectricCar的父类的方法__init__()，让ElectricCar实例包含父类的所有属性。父类也称为超*
     *类（superclass），名称super因此而得名。*

   - **在继承中子类既可以使用父类的属性，也可以自己创建新的属性，同时可以将父类中的方法进行重写，python将会只使用你重写的方法**

   - *将实例用作属性，使用代码模拟实物时，你可能会发现自己给类添加的细节越来越多：属性和方法清单以及文件都越来越长。在这种情况下，可能需要将类的一部分作为一个独立的类提取出来。你可以将大型类拆分成多个协同工作的小类。*

   - **导入类**：Python允许你将类存储在模块中，然后在主程序中导入所需的模块。

     **from <文件名> import <类名>**    导入一个类名,文件名即模块名

     **from<文件名>import<类名1>,<类名2>**  导入多个类名

     **import <文件名>**   导入整个模块

     使用时直接调用**<模块名>.<类名>**

   - **python标准库**：Python标准库是一组模块，安装的Python都包含它。可以开始使用其他程序员编写好的模块了。可使用标准库中的任何函数和类，

   - **类编码风格**：类名都采用小驼峰命名法，即将类名中的每个单词的首字母都大写，而不使用下划线。实例名和模块名都采用小写格式，并在单词之间加上下划线。

     *对于每个类，都应紧跟在类定义后面包含一个文档字符串。这种文档字符串简要地描述类的功能，并遵循编写函数的文档字符串时采用的格式约定。每个模块也都应包含一个文档字符串，对其中的类可用于做什么进行描述*

5. 文件

   - 读取文件内容：

     *函数open()接受一个参数：要打开的文件的名称。Python在当前执行的文件所在的目录中查找指定的文件。在这个示例中，当前运行的是file_reader.py，因此Python在file_reader.py所在的目录中查找pi_digits.txt。函数open()返回一个表示文件的对象。在这里，open('pi_digits.txt')返回一个表示文件pi_digits.txt的对象；Python将这个对象存储在我们将在后面使用的变量中。关键字with在不再需要访问文件后将其关闭。在这个程序中，注意到我们调用了open()，但没有调用close()；你也可以调用open()和close()来打开和关闭文件，但这样做时，如果程序存在bug，导致close()语句未执行，文件将不会关闭。这看似微不足道，但未妥善地关闭文件可能会导致数据丢失或受损。如果在程序中过早地调用close()，你会发现需要使用文件时它已关闭，这会导致更多的错误。并非在任何情况下都能轻松确定关闭文件的恰当时机，但通*过使用前面所示的结构，可让Python去确定：你只管打开文件，并在需要时使用它，Python自会*在合适的时候自动将其关闭。有了表示pi_digits.txt的文件对象后，我们使用方法read()（前述程序的第2行）读取这个文件的全部内容，并将其作为一个长长的字符串存储在变量contents中。这样，通过打印contents*的值，就可将这个文本文件的全部内容显示出来。*

     with函数只能在其中使用数据，但可以将数据存入字符串中再调用

   - *写入文件：调用open()时提供了两个实参。第一个实参也是要打开的文件的名称；*
     *第二个实参（'w'）告诉Python，我们要以写入模式打开这个文件。打开文件时，可指定读取模*
     *式（'r'）、写入模式（'w'）、附加模式（'a'）或让你能够读取和写入文件的模式（'r+'）。如果*
     *你省略了模式实参，Python将以默认的只读模式打开文件。如果你要写入的文件不存在，函数open()将自动创建它。**然而，以写入（'w'）模式打开文件时千万要小心，因为如果指定的文件已经存在，Python将在返回文件对象前清空该文件。**，我们使用文件对象的方法write()将一个字符串写入文件。这个程序没有终端输出，将看到其中包含内容，**Python只能将字符串写入文本文件。要将数值数据存储到文本文件中，必须先使用函数***
     ***str()将其转换为字符串格式。***

   - *异常:**try-except-else**代码块的工作原理大致如下：Python尝试执行try代码块中的代码；只有可*
     *能引发异常的代码才需要放在try语句中。有时候，有一些仅在try代码块成功执行时才需要运行*
     *的代码；这些代码应放在else代码块中。except代码块告诉Python，如果它尝试运行try代码块中*
     *的代码时引发了指定的异常，该怎么办。*
     *通过预测可能发生 错误的代码，可编写健壮的程序，它们即便面临无效数据或缺少资源，也*
     *能继续运行，从而能够抵御无意的用户错误和恶意的攻击*

     ***方法split()**以空格为分隔符将字符串分拆成多个部分，并将这些部分都存储到一个列表中。*
     *结果是一个包含字符串中所有单词的列表，虽然有些单词可能包含标点。*

   - ***存储数据：一种简单的方式是使用模块json来存储数据。***
     *模块json让你能够将简单的Python数据结构转储到文件中，并在程序再次运行时加载该文件*
     *中的数据。更重要的是，JSON数据格式并非Python专用的。*

     ***json.dump() 存储数据, json.load()读取数据***

6. 测试函数：

   - 使用Python模块unittest中的工具来测试代码
   - 针对类的测试函数

   - ```python
     import unittest 
     from name_function import get_formatted_name 
     	class NamesTestCase(unittest.TestCase): 
      """测试name_function.py""" 
      
      def test_first_last_name(self): 
      """能够正确地处理像Janis Joplin这样的姓名吗？""" 
      	formatted_name = get_formatted_name('janis', 'joplin') 
      	self.assertEqual(formatted_name, 'Janis Joplin') 
     unittest.main() 
     ```

   - 针对类的测试函数

   - 断言方法检查你认为应该满足的条件是否确实满足。如果该条件确实满足，你对程序行为的假设就得到了确认，你就可以确信其中没有错误。如果你认为应该满足的条件实际上并不满足，Python将引发异常。

   - 断言方法![image-20210321151242730](C:\Users\li chun jian\AppData\Roaming\Typora\typora-user-images\image-20210321151242730.png)

   - 

7. 项目实践：

   - 

 

l