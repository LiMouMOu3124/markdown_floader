1. SyntaxError: (unicode error) 'unicodeescape' codec can't decode bytes in position 2-3: truncated \UXXXXXXXX escape

   错误原因：转义问题，在windows系统当中读取文件路径可以使用\,但是在python字符串中\有转义的含义，如\t可代表TAB，\n代表换行，所以我们需要采取一些方式使得\不被解读为转义字符。

   解决方案：1、在路径前面加r，即保持字符原始值的意思。

   ​						sys.path.append(r'c:\Users\mshacxiang\VScode_project\web_ddt')
   ​					2、替换为双反斜杠

   ​						sys.path.append('c:\Users\\mshacxiang\VScode_project\web_ddt')
   ​					3、替换为正斜杠

   ​						sys.path.append('c:/Users/mshacxiang/VScode_project/web_ddt')

   

