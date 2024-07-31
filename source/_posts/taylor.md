---
title: 泰勒展开公式推导
tags:
  - Taylor
categories: Algorithms
date: 2024/3/29
abbrlink: 48d1
---
**这个教程会以简单易懂的方式推导泰勒展开公式。**
<!--more-->

 <span>0. 变限积分求解</span>

$$\large \int_{0}^{x} \int_{0}^{x} \int_{0}^{x} 1 \\, dx \\, dx \, dx = \, ?$$

$$\text{先解最内层变限积分：}$$

$$\large  \int_{0}^{x} 1 \, du = u \Big|_{0}^{x} = x - 0 = x $$

$$\text{将最内层变限积分的解带入第二层积分：}$$

$$\large  \int_{0}^{x} \int_{0}^{x} x \, dx \, dx = \, ?$$

$$\text{再解第二层变限积分：}$$

$$\large  \int_{0}^{x} x \, dx = \frac{1}{2!}x^2\Big|_{0}^{x} $$

$$\text{把积分符号内的x看作u: }$$

### $$\large  \int_{0}^{x} u \, du = \frac{1}{2!}u^2\Big|_{0}^{x} $$

$$\text{求解：}$$

\large  \frac{1}{2!}u^2\Big|_{0}^{x} = \frac{1}{2!}x^2 - \frac{1}{2!}(0)^2 

$$\text{得出第二层变限积分结果为：}$$

$$\large  \frac{1}{2!}x^2 $$

$$\text{将第二层变限积分的解带入最外层积分：}$$
$$\large  \int_{0}^{x} \frac{1}{2!}x^2 \, dx = \, ?$$
$$\text{解最外层变限积分：}$$
$$\large  \int_{0}^{x} \frac{1}{2!}x^2 \, dx = \frac{1}{3!}x^3\Big|_{0}^{x} $$
$$\text{把积分符号内的x看作u: }$$
$$\large  \int_{0}^{x} \frac{1}{2!}u^2 \, du = \frac{1}{3!}u^3\Big|_{0}^{x} $$
$$\text{得出最外层变限积分结果为：}$$
$$\large  \frac{1}{3!}x^3 - \frac{1}{3!}(0)^3 = \frac{1}{3!}x^3 $$

 <span> 1. 泰勒公式推导</span>

$$\large f(x) = \int_{c}^{x} f'(x) \, dx + f(a)$$
$$\large f'(x) = \int_{c}^{x} f''(x) \, dx + f'(a)$$
$$\large f''(x) = \int_{c}^{x} f'''(x) \, dx + f''(a)$$
$$\large f'''(x) = \int_{c}^{x} f^{(4)}(x) \, dx + f'''(a)$$

f(x) = ∫_{c}^{x} f'(x) \, dx + f(a)  
f'(x) = ∫_{c}^{x} f''(x) \, dx + f'(a)  
f''(x) = ∫_{c}^{x} f'''(x) \, dx + f''(a)  
f'''(x) = ∫_{c}^{x} f^{(4)}(x) \, dx + f'''(a)



 原函数的信息=导函数的信息积分+初始值
$$\large f(x) = \int_{c}^{x} \left( \int_{c}^{x} \left( \int_{c}^{x} \left( \int_{c}^{x} f^{(4)}(x) \, dx + f'''(a) \right) \, dx + f''(a) \right) \, dx + f'(a) \right) \, dx + f(a)$$

$$\large f(x) = \int_{c}^{x} \left( \int_{c}^{x} \left( \int_{c}^{x} \left( \int_{c}^{x} f^{(4)}(x) \, dx + f'''(a) \right) \, dx \right) \, dx + f''(a) \right) + \frac{f'(a)}{1!} \cdot (x-c)^1 + f(a)$$


$$\large f(x) = \int_{c}^{x} \left( \int_{c}^{x} \left( \int_{c}^{x} \left( \int_{c}^{x} f^{(4)}(x) \, dx \right) \, dx + f'''(a) \right) \, dx + \frac{f''(a)}{2!} \cdot (x-c)^2 + \frac{f'(a)}{1!} \cdot (x-c)^1 + f(a) \right) \, dx$$

$$\large f(x) = \int_{c}^{x} \left( \int_{c}^{x} \left( \int_{c}^{x} \left( \int_{c}^{x} f^{(4)}(x) \, dx \right) \, dx + \frac{f'''(a)}{3!} \cdot (x-c)^3 + \frac{f''(a)}{2!} \cdot (x-c)^2 + \frac{f'(a)}{1!} \cdot (x-c)^1 + f(a) \right) \, dx \right)$$

$$\text{以此类推，前面剩余的积分为余项，后面为泰勒展开公式。}$$

$$\large f(x) = f(a) + \frac{f'(a)}{1!} \cdot (x-c)^1 + \frac{f''(a)}{2!} \cdot (x-c)^2 + \frac{f'''(a)}{3!} \cdot (x-c)^3 + \ldots$$

 <span> End. </span>
 如内容有错误或不明确的地方欢迎联系我进行更正！

$$\large f(x) = \int_{c}^{x} f'(x) \, dx + f(a)
$$
$$
\large f'(x) = \int_{c}^{x} f''(x) \, dx + f'(a)
$$
$$
\large f''(x) = \int_{c}^{x} f'''(x) \, dx + f''(a)$$
$$\large f'''(x) = \int_{c}^{x} f^{(4)}(x) \, dx + f'''(a)$$

$x^2+y^2=z^2$



$$ \huge \int_{0}^{x} \int_{0}^{x} \int_{0}^{x} 1 \, dx \, dx \, dx = \, ? $$