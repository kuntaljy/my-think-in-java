# My Think in Java
## Why should you have minimum scope for variables?
变量作用域越大，修改时涉及的面越广，变更引起的风险扩散也就越大。
## Why should you understand performance of String Concatenation?
String是final类型，每次改变都会生成新的对象，大量字符串拼接可能会引起性能下降。Java8中的字符串拼接会默认转换为StringBuilder拼接，避免产生大量String对象
## What are the best practices with Exception Handling?
1.	尽早throw尽晚catch
2.	使用try-with-resource，自动释放资源
3.	抛出异常和捕获异常时都应该使用明确的异常类型而不是通用类型
4.	捕获异常是为了处理异常，或者用自定义异常封装原始异常，不要在捕获异常后什么也不处理把异常影藏起来
## When is it recommended to prefer Unchecked Exceptions?
除了记录日志以外没有其他办法处理的异常可以考虑使用Unchecked Exception
## When do you use a Marker Interface?
没有任何方法的接口为Marker Interface，可以用于对子类进行标记以便区别对待。
## Why are ENUMS important for Readable Code?
枚举可以定义数据的名称，用于替换魔鬼数字(字符)使得程序可读性更高
## Why should you minimize mutability?
尽可能地限制类的可变性，可以减少对象存在的状态数量，可以更容易地分析对象，以及降低出错的可能性。
## What is functional programming?
将行为作为数据传递
## Why should you prefer Builder Pattern to build complex objects?
当我们创建一个对象需要判断大量条件和参数时，与其提供带有大量参数的、各种不同重载方式的构造函数（其中可能有部分必传参数部分可选参数），倒不如为它专门提供一个Builder类来负责处理这些创建逻辑
## Why should you avoid floats for Calculations?
浮点数计算为丢失精度，在高精度要求的场景下可能引起严重的问题
## Why should you build the riskiest high priority features first?
1.	风险可控
2.	尽早暴露问题
3.	Fail fast
