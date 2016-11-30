# vimscript

## summary
## memo
1. echo $MYVIMRC 命令显示文件的位置及名称
2. 使用"进行注释
3. 使用前缀leader来设置自己的映射,例:let mapleader = ","
4. 自动命令：autocmd BufNewFile * :write
                        ^       ^   ^
												|				|		|
												|				|		要执行的命令
												|				|
												|				用于事件过滤的模式
												|
												要监听的事件
5. 把自动命令放到组中augroup,如果想清除一个组，可以把autocmd!包含在组中
6. Operator-Pending映射,当想搞清楚怎么定义一个新的Operator-pending movement的时候，可以从下面几个步骤来思考
	1)在光标所在的位置开始
	2)进入可视模式
	3)...把映射的键放在这里...
	4)所有你想包含在movement中的文字都会被选中
7. :normal命令的后面会跟着一串字符串，就像在常用模式下敲击字符串一样,但是normal不能识别特殊字符,比如<cr>
8. vim中的变量和选项:变量可以使用let xx="xx"来设置，引用选项则使用&符号,比如let &textwidth=80
9. 设置局部选项，则使用let &1:number=1的样子
10.设置寄存器使用@符号，比如let @a="hello"
11.当在变量中加入b:,比如let b:hello="world",这相当与是当前缓冲区的本地变量
12.大小写不敏感操作符:==?,==#大小写敏感比较符
13.没有作用域限制的Vimscript函数必需以一个大写字母开头，调用函数使用call xxx()
14.在写需要参数的Vimscript时，你总需要给参数加上a:,来告诉Vim去参数作用域中查找
15.函数定义中的...说明这个函数可以接受任意数目的参数，不能对列表使用echom
15.不能对函数的参数变量从新赋值
16..是vim中的连接运算符
17.^@在vim中表示换行符
18.字符串函数
19.在字符串中\<esc>表示转到normal模式
20.

