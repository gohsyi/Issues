# Issues I encoutered using CPLEX to solve linear programmings

### _External data element "" was not defined._

.dat文件里没加分号

------

### _Indexing array "" with type dvar int not supported by this algorithm_

用变量去index一个常量array的时候就会出现这个错误，可以将变量升维成onehot，然后乘上常量array得到相同的结果。

https://www.ibm.com/developerworks/community/forums/html/topic?id=77777777-0000-0000-0000-000014943610

------

### _Cplex cannot extract expression_

往往是表达式里包含子表达式相乘，子表达式里又包含相乘，总的次数会变成二次，所以报错。

https://developer.ibm.com/answers/questions/372036/cplex-cannot-extract-expression/

------

### _CPLEX Error 1016: Restricted version. Problem size limits exceeded._

一个01变量和另一个变量相乘，直接乘的话会出现这个错误，用下面的方法转化一下。

https://orinanobworld.blogspot.com/2010/10/binary-variables-and-quadratic-terms.html

------
