# jsProject
jsRefactoring代码重构学习，使用《重构 改善既有代码的设计》（第二版）学习笔记

1.4.1 将statement里面的函数提炼出来，将计算戏剧费用的代码提炼为函数，amountFor（）
1.4.1 将amountFor（）函数中返回值的变量修改为result
1.4.2 javascript 动态语言的参数取名字时都默认带上其类型名，一般我会使用不定冠词a，本次重构，就将amountFor（）函数中的perf修改为aPerformances 
1.4.3 很多局部作用域的临时变量，应该及时移除，重构手法叫“以查询取代临时变量”，也就是说通过其他变量的查询操作可以获得该变量，那么就可以将该变量移除。比如这里的play是为了获取计算戏剧的费用的局部作用区域变量。所以可以通过aPerformance变量查询获得。
1.4.4 使用内联变量手法内联play变量
1.4.5 amountFor（）函数内部应用新提炼的函数，最后删除playFor(perf)参数。