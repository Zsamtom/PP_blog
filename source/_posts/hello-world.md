---
title: Hello World
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).
### 变量

计算机中的存储空间，用于保存数据

```python
定义变量的格式
变量名 = 值
注意：= 是赋值运算符，左右两边打上空格是为了代码的规范性，美观性。
```

```python
numl = 3  #numl就是一个变量，保存可乐的价格
num2 = 10   #num2也是一个变量，保存冰淇淋的价格
total= num1 + num2 #total也是一个变量，保存总价格

a = 999	# 一个变量可以反复赋值,并且可以是不同的数据类型
```

```python
print (numl)
# 加上引号会打印引号里面的内容，没有引号就会被识别成变量名，打印的是变量的值，如果该变量没有被赋值，就会报命名错误
变量只有再赋值以后才会被创建，所以使用变量之前必须要赋值
```

`注意事项：首次使用变量会在内存中划分空间，并初始化值再次使用变量不再划分空间修改原空间的值。`

### 2 标识符

含义：程序员定义变量名、函数名

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)

