# Python算法：map&reduce
map()接收一个函数，一个Iterable，将传入的函数依次作用到序列的每个元素，并把结果作为新的Iterator返回。

ps.

    可作用于for循环的对象都是Iterable类型；
    可作用于next()函数的对象都是Iterator类型，它们表示一个惰性计算的序列；
    集合数据类型如list、dict、str等是Iterable但不是Iterator，不过可以通过iter()函数获得一个Iterator对象；
    Python的for循环本质上就是通过不断调用next()函数实现的。
reduce把一个函数作用在一个序列[x1,x2,x3,...]上，这个函数必须接收两个参数，reduce把结果继续和序列的下一个元素做累积计算。

 

    例：把字符串转换成浮点数

             return reduce(lambda x, y: x + y / (10 ** len(str(y))), map(int, s.split('.')))     
