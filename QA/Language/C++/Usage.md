# C++用法
### 1. Lambda函数
#### 1.1 适用版本
C++11及之后的版本
#### 1.2 用处
一种方便参数传递和定义匿名函数的方法。常用于封装算法、执行异步方法。
#### 1.3 如何使用
[掘金连接](https://juejin.cn/post/6866993564346384397)
##### 1.3.1 表达式组成
样例代码
~~~C++
int main() {
    std::vector<int> nums = {1, 5, 3, 4, 2, -1, 10};
    std::sort(nums.begin(), nums.end(), [](int a, int b) mutable throw() -> bool {
        // lambda 表达式函数体，在这里做到了将输入数组升序排列
        return (std::abs(a) < std::abs(b));
    });
    for (int i : nums) std::cout << i << " ";
    // >: 1 -1 2 3 4 5 10
}
~~~
上述排序代码中`[](int a, int b) mutable throw() -> bool {}`为lambda表达式最原始内容
1. `[]`捕获子句(引导子句)：用来捕获周围范围中出现的变量(需要使用的外部变量)，可以在其中声明获取的变量是按值访问还是引用访问，默认是不捕获外部变量`[&]`
> 
2. `()`参数列表：用来获取参数，与普通函数类似
3. `mutable`可变类型（可选）：一般来说，在`lambda`体中调用运算符的变量是以`const`来使用；`mutable`可让const变量可以被修改
4. `throw()`异常类型（可选）：和普通函数一样可以引发异常，如果不引发异常，则声明`noexcept`
5. `->bool`返回类型（可选）
6. `{}`函数体
